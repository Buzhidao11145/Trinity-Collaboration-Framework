# 即用型模板：IPA修改一键流程

> **触发语句：** "龙虾，把这个IPA改了，注入xxx.dylib"
> **创建时间：** 2026-06-01
> **所属框架：** Trinity v1.0
> **标准化流程来源：** IPA修改决策规则

---

## 一句话启动

```
龙虾，把这个IPA改了[来自<路径>]，注入<xxx.dylib>，重签名为<证书>，导出到<目标路径>
```

## 自动执行流程

### 1️⃣ 原版文件验证

```bash
ls -lh <IPA路径>
file <IPA路径>
ditto -x -k <IPA路径> <解压目录>
```

### 2️⃣ 修改前检查清单

- [ ] 原版IPA大小是否与预期一致？
- [ ] 解压后Payload目录是否存在？
- [ ] 目标dylib是否存在并可读？

### 3️⃣ ditto解压

```bash
ditto -x -k <原版IPA> <工作目录>
```

### 4️⃣ 注入dylib

```bash
optool install \
    -c load \
    -p @executable_path/<dylib文件名> \
    -t <Payload>/<App>/
```

### 5️⃣ 重签名

```bash
codesign -f -s <证书名> <Payload>/<App>/
```

### 6️⃣ ditto打包

```bash
ditto -c -k <工作目录>/Payload <输出IPA名称>
```

### 7️⃣ 完整性校验

```bash
# 大小校验：修改后 >= 原版 ✅，< 原版 ❌
ls -lh <输出IPA>
ls -lh <原版IPA>

# 签名验证
codesign -dvvv <Payload>/<App>/<AppBinary> 2>&1 | grep "Authority"
```

## 常见问题即答

| 问题 | 回答 |
|:----|:-----|
| "用zip/unzip行不行？" | ❌ 禁用！必须用ditto。 |
| "哪个是原版？" | 按大小验证，App Store原版 > 180MB（参考实战数据）。 |
| "注入后App闪退？" | 检查dylib架构是否匹配（lipo -info）。 |
| "签名失败？" | 确认证书是否存在于钥匙串，`security find-identity -v -p codesigning`。 |

---

*参考：`skills/ipa-modifier/SKILL.md` 完整操作流程。*
