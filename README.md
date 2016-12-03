# webpack_dev_server161014

webpack-dev-server支持2种自动刷新的方式：    
1. Iframe模式  
2. Inline模式  

Inline模式下，访问路径：http://localhost:8080/  

Iframe模式下，访问路径：http://localhost:8080/webpack-dev-server/index.html  

Iframe模式与Inline模式比较：  

Iframe模式 特点：    
1. 配置不需要改变；  
2. 提示信息在页面顶部；  
3. URL的变化不反应在浏览器的地址栏上。    

Inline模式：    
要想使用Inline模式，需要配置以下其一：    
1. 在命令行指定 --inline 参数；    
2. 在webpack.config.js中配置：devServer: { inline: true }  
Inline模式 特点：    
1. 需要配置上面说明的内容；  
2. 状态信息在控制台显示；  
3. URL的变化反应在浏览器的地址栏上。  

提示：    
1. Iframe模式下，也可以在命令行中指定 --inline 参数，此时状态信息除了在页面顶部显示，也在控制台显示。  
2. 执行npm run start，查看执行情况。    
3. webpack-dev-server默认端口是8080。

webstorm修改文件，webpack-dev-server不自动编译刷新的解决办法：  
“设置”--“系统设置”，选项“Use "safe write"(save changes to a temporary file first)”，不打勾。
