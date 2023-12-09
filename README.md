UUID :  08374876-37a1-4302-a9e3-196f1ba17e6b


无需域名 通过cloudflare部署vless节点+tls+443端口

#   1. 在github新建一个存储库 上传_worker.js

#   2.  登录cloudflare,点击 Workers 和 Pages

#   3.  创建应用程序 ， 选择Pages ，链接你的GitHub新创建的仓库_worker.js---点击部署

#   4.  部署完成 ，点击域 ，进入第二个页面，在链接地址后面输入 /“你的UUID”  回车  你的vless节点就出来了  如下显示


==========================配置详解==============================

################################################################

CF-pages-vless+ws+tls节点，分享链接如下：

vless://你的UUID@jianxian.xyz:443?encryption=none&security=tls&type=ws&host=cloudflare自带的三级域名&sni=cloudflare自带的三级域名&fp=random&path=%2F%3Fed%3D2048#cloudflare自带的三级域名

---------------------------------------------------------------

注意：如果 github-be5.pages.dev 在本地网络打不开（中国移动用户注意）
       客户端选项的伪装域名(host)必须改为你在CF解析完成的自定义域名
       
---------------------------------------------------------------

客户端必要文明参数如下：


客户端地址(address)：自定义的域名 或者 优选域名 或者 优选IP（反代IP必须与反代端口对应）

端口(port)：6个https端口可任意选择(443、8443、2053、2083、2087、2096)

用户ID(uuid)：你的uuid

传输协议(network)：ws 或者 websocket

伪装域名(host)：cloudflare自带的三级域名

路径(path)：/?ed=2048

传输安全(TLS)：开启

跳过证书验证(allowlnsecure)：false

################################################################
