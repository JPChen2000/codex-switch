# codex-switch

快速切换和管理 `~/.codex` 目录下的 Codex 配置文件。

## 一键安装

```bash
curl -fsSL https://github.com/JPChen2000/codex-switch/codex-switch -o ~/.local/bin/codex-switch && chmod +x ~/.local/bin/codex-switch
```

安装到你使用的PATH路径，例如 `~/.local/bin/codex-switch`
如果安装后任然找不到指令，请检查是否添加了PATH环境变量。

## 用法

```bash
codex-switch                           # 列出可用 key
codex-switch  <key>                     # 切换到指定配置
codex-switch  --list, -l                # 列出可用 key
codex-switch  --save <key>              # 保存当前配置为新 key
codex-switch  --show                    # 显示当前 base_url 和 api_key
codex-switch  --base_url -api_key      # 更新 base_url 和 api_key（不改 bak）
codex-switch  --base_url --api_key --save  # 更新并保存为新配置
codex-switch  --rm <key>               # 删除指定配置
```

## 示例

```bash
# 切换
codex-switch <key>

# 查看当前配置
codex-switch --show
# base_url : https://xxxx/v1
# api_key  : sk-xxxxx

# 保存
codex-switch --save my-config

# 创建新配置
codex-switch --base_url "https://api.example.com/v1" --api_key "sk-key" --save newprovider

# 删除
codex-switch --rm old-config
```
