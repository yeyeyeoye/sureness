## url路径匹配  

我们配置的资源格式为：`requestUri===httpMethod`, 即请求的路径加上其请求方式(`post,get,put,delete...`)作为一个整体被视作一个资源   
`eg: /api/v2/book===get` `get`方式请求`/api/v2/book`接口数据  
这里的`requestUri`支持url路径匹配:  *, **  

通配符                      | 描述              
---                        | ---               
*                          | 匹配0个或1个目录   
**                         | 匹配0个或多个目录  


 样例                      | 说明  
 ---                       | ---
 /api/*/book               | 可以匹配 /api/user/book 或 /api/book等  
 /**                       | 可以匹配任何路径  
 /**/foo                   | 可以匹配 /api/user/book/foo 等  
 
匹配优先级: 原始字符串 大于 * 大于 **
