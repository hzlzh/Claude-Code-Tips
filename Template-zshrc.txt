# Claude Code 实用小技巧(2) by @hzlzh

# cc -c 继续上次对话 | cc -r 选择近期对话
alias cc='claude'

# 纯聊天模式：禁用所有工具，节省 Token 且更安全
alias cchat='claude --tools ""'

# YOLO模式：AI自动驾驶，不再询问Approve?，临时用，注意风险
alias ccyolo='claude --dangerously-skip-permissions'

# 个性化一键直达项目 & cc
alias ccll='cd ~/Product/git/Lock-Launcher && claude'
alias cc2c='cd ~/Product/git/TwoCamera && claude'
alias ccmx='cd ~/Product/git/MenubarX && claude'
alias ccsx='cd ~/Product/git/StickerX && claude'

# 更多工具

# Emoji联想：根据输入推荐相关性最高的 5 个 Emoji
ccemoji() { claude -p "Output 5 Emojis with highest relevance to: $*"; }

# 终端指令翻译：cchelp 查找所有大于 100MB 的文件
cchelp () { claude -p "Only output the shell command to do: $*"; }

# 自动命名建议：纠结变量名/函数名？ccname 直接给灵感
ccname() { claude -p "Output 5 best naming options for: $*"; }

# 正则速成：ccregex 匹配所有的域名
ccregex() { claude -p "Only output the regex pattern for: $*"; }
