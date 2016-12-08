### 前言
之前有很多人问我能否开放天天云搜的搜索接口，考虑到自己的服务器太垃圾，怕用的人太多服务器受不了，毕竟查询什么的比较耗资源，所以一直没答应，虽然我发现有人通过对云搜网盘助手进行抓包从而获取api接口，但毕竟影响不大，所以我也一直没封（要封也很容易，建议大家不要再用那个接口，我迟早会把它封掉的！！！），扯了这么多废话我只想告诉大家一个好消息：最近由于服务器升级，加之对查询稍微做了点优化，本屌决定免费开放搜索接口！

### 用途
大家可以将接口写到自己的软件中，从而实现资源查找的功能，同样也可用于QQ机器人、微信公众号等的资源查询（需二次开发，自行解决，本人不提供任何技术支持），本接口仅供大家学习与交流，不保证接口的稳定性和长久性，免费使用，不提供任何收费服务

### 调用说明
接口地址：http://api.ygyhg.com/pc/free?keyword=hello&order=feedtime&num=3

参数说明：

keyword：关键字，不能为空

order：排序方式，可不写，默认综合排序，feedtime是按分享时间倒序排列，size是按文件大小排序（从大到小）

num：返回最大的结果数，可不写，默认为10个，目前最多只能返回30个

返回结果为json数据，示例如下：

```
{"error":0,"counts":6003,"content":[{"id":"10840829","title":"C-ute - Alo-Hello!3 C-ute Blu-ray Disc.iso","size":"21779447808","type":"5","feedtime":"1440223500575","url":"http:\/\/pan.baidu.com\/share\/link?uk=327121&shareid=3506677279"},{"id":"6245974","title":"Hello! Project SATOYAMA movement MUSIC VIDEO CLIPS.ISO","size":"7950049280","type":"5","feedtime":"1386658270000","url":"http:\/\/pan.baidu.com\/share\/link?uk=4178108009&shareid=2807878792"},{"id":"11230000","title":"Hello! Project \u91ce\u97f3\u30d7\u30ec\u30df\u30a2\u30e0LIVE \uff5e\u5916\u30d5\u30a7\u30b9\uff5esupported by Hellosmile\u3008BD Rip Ver.\u3009.mkv","size":"7459222886","type":"2","feedtime":"1384070580000","url":"http:\/\/pan.baidu.com\/share\/link?uk=3591931869&shareid=1736882787"}]}
```

参数说明：

error：错误代码，0为正确，其他为错误

counts：总共的资源数量，部分资源可能为0（表示服务器上暂时没有收录该资源）

content：资源内容，无资源则为空

title：资源名称

size：大小，单位为byte

feedtime：分享时间，时间戳

url：资源地址

如果请求错误会返回错误信息


```
{"error":2,"content":"keyword\u4e0d\u80fd\u4e3a\u7a7a\uff01"}
```

error：错误代码，大于0

content：错误原因

### 最后几句
由于是免费服务，希望大家不要滥用，对于单IP请求过于频繁的可能会被系统拦截，本人承诺该接口在服务器吃的消的情况下会一直免费提供服务，如果服务器超载会临时或者长久暂停服务，恕不另行通知！天天云搜：https://so.ygyhg.com（建议添加收藏夹哦，重要信息也会在本页面更新）