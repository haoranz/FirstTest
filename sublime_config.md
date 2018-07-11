# sublime_config 
## Settings - Syntax Specific
```
{   
    "font_size": 15,
    "tab_size": 4, 
    "translate_tabs_to_spaces": true,
    "trim_trailing_white_space_on_save": true, 
    "ensure_newline_at_eof_on_save": true,
    "word_wrap": true,
}
```
## SublimeLinter 语法检查
1. Install Flake8 第三方代码检查组件
`pip install flake8`
2. Install SublimeLinter
```
SublimeLinter
SublimeLinter-flake8
```
3. CONFIG
```
// SublimeLinter Settings - User
{
    // 代码检查结果延时显示
    "delay": 0.8,
    "lint_mode": "background",
    "linters": {
        "flake8": {
            //语法检查忽略：E501 单行不超过79字符 
            "args": ["--ignore=E501"],
        }
    },    
    // 提示样式
    "styles": [
        {
            "scope": "region.yellowish markup.warning.sublime_linter",
            "types": ["warning"]
        },
        {
            "priority": 1,
            "icon": "circle",
            "mark_style": "solid_underline",
            "scope": "region.redish markup.error.sublime_linter"
        }
    ],
}
```
4. 重启Sublime  

## Anaconda 代码补全  
1. 配置 避免和flake8冲突
```
{
    "anaconda_linting": false,
    "pep8": false
}
```

## Sider 增强
1. sidebarenhancements

## Syntax HighLight
- babel
- PrettyJSON 