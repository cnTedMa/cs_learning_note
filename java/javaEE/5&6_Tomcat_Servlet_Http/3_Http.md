# HTTP:
* 概念: Hyper Text Transfer Protocol超文本传输协议
  * 传输协议: 定义了客户端和服务器端通信时, 发送数据的格式
  * 特点:
    1. 基于TCP/IP的高级协议
    2. 默认端口80
    3. 基于请求/响应模型的: 一次请求对应一次响应
    4. 无状态的: 每次请求之间相互独立, 不能交互数据
  * 历史版本:
    * 1.0: 每一次请求响应都会建立新的连接
    * 1.1: 复用连接
* 请求消息数据格式
  1. 请求行
     
     请求方式 请求url 请求协议/版本 GET /login.html HTTP/1.1
     * 请求方式:
       * HTTP协议有7种请求方式, 常用的有2种
         * GET: 
            1. 请求参数在请求行中, 在url后
            2. 请求的url长度有限制
            3. 不太安全
         * POST: 
             1. 请求参数在请求体中
             2. 请求长度没有限制
             3. 相对安全
  2. 请求头
     
     请求头名称: 请求头值
     * 常见的请求头:
       1. User-Agent: 浏览器版本信息
          * 作用: 解决不同浏览器兼容问题
       2. Referer: 请求来自哪里
          * 作用:
            1. 防盗链
            2. 统计工作
  3. 请求空行
  
     空行
     * 作用: 用于分割POST请求请求头和请求体
  4. 请求体
* 响应消息数据格式