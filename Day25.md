# 代码片段
- tab 切换输出位置
- esc 取消
- cammand + i 展示提示
# 不爽
- tab 切换位置后需要重新使用 i/a 进入编辑模式
# 自定义代码片段
```json
{
	"Print to console": { // 名称	
		"scope": "javascript,typescript", // 生效语言 
		"prefix": "log", // 关键字
		"body": [ // 具体内容 其中 $1 是 tab 位置
			"console.log('%c------------ start [${2:$1}] -------------','color:purple');", 
			"console.log($1);", // $1:默认值 // $1|选项1,选项2,选项3| // $1:$2
			"console.log('%c------------ end [${2:$1}] ---------------','color:purple');",
			"$3"
		],  
		"description": "Log output to console" // 描述
	}  
}
```