# DangerousSpamWords
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdudy5%2FDangerousSpamWords.svg?type=shield)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdudy5%2FDangerousSpamWords?ref=badge_shield)

:notes:最轻的敏感词库，低误识别率  
80%的命中率，精简的内容，大大减小服务器负担，不再需要遍历一个数万行的文本了

**欢迎Pull request帮助大家收集一个最强大的敏感词字典！**

全部敏感词经过人工筛选，将正常词语误识别为敏感词的几率极小，完全不影响日常交流使用。  
仅过滤**政治敏感**与**色情粗暴**词语，不包含部分隐晦词语。

用**Java**套用本字典并输出结果、命中敏感词汇、词典版本、运行花费时间请看**SpamReader**:
https://github.com/AdlerED/SpamReader

API接口地址:  
https://www.stackoverflow.wiki/spam.do  
你可以使用GET或POST方法向服务器发送数据  
要求参数:  
**words**: 需要过滤敏感词的内容  
**replaceTo**: 将敏感词汇替换为指定内容  
注意事项:  
发送的数据需要使用URLEncoder进行编码, 否则可能会出现问题  
返回结果:  
服务器会返回json的结果  
**Result**: 过滤结果  
**SpamHits**: 命中敏感词汇  
**SpamWordsVersion**: 词典版本  
**Runtime**: 运行花费时间  
示例页面:  
https://www.stackoverflow.wiki/spam.do?words=sb&replaceTo=*  
可能出现的问题:  
如果内容含有HTML标签, 浏览器转换后可能会直接将其解析为HTML标签, 所以可以使用JS的innerText()方法和JQuery的text()方法显示原始结果.  


## License
[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fdudy5%2FDangerousSpamWords.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fdudy5%2FDangerousSpamWords?ref=badge_large)