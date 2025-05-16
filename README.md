##### 目标网站：`https://www.shireyishunjian.com/main/`  需要梯子才可以访问
##### 用途：个人留档，整理一下训练AI玩，`H成人向网站`，介意的可以不用看了。
##### 工期、报价：个人爱好非商业用途，三方比价，请直接报工期和报价。
##### 交付形式和付款形式：闲鱼预付50%→交付全部爬好的json数据→确认收货→付尾款50%→交付可运行代码→本地部署通过→确认收货
##### 运行环境：win11专业版或者 Ubantu 22.4，Cpu i7-13700K，内存96G 
##### 网站需要登录，登录账号：`gdasgasgd`    密码：`123456789`

### 爬虫需求：
1 进入网站登录后，需要爬取红色窗口（直播、尿裤子 憋尿、AB DL、拉裤子 浣肠、湿热＋、周边）下所有子目录（蓝色，交友、小说、绘画、尿裤子|憋尿讨论区）
[![ ](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516192937.png?raw=true " ")](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516192937.png?raw=true " ")
2 以湿热一瞬间»论坛列表›尿裤子|憋尿›尿裤子|憋尿小说区›即使我不再是15岁。(第二卷)为例子，网址：`https://www.shireyishunjian.com/main/forum.php?mod=viewthread&tid=265287&page=1#pid3411069`
需要采集红色窗口的数据，包括帖子名称、主题、每一层的发帖人、发帖时间、发帖内容、帖子楼层号，注意是贴子里每一层楼的内容。
[![  ](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516194232.png?raw=true "  ")](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516194232.png?raw=true "  ")
[![](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516194318.png?raw=true)](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516194318.png?raw=true)
3 特殊情况
[![ ](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516194604.png?raw=true " ")](https://github.com/suqing7878/-/blob/main/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20250516194604.png?raw=true " ")
帖子中包含图片，需要保存图片的url，存在多个图片的时候保存格式`[“img1”,”img2”]`,具体如下案例
4 数据保存格式
保存为json文件，每个帖子一个独立的json文件，案例格式：
```json
{
    "帖子名称":"自購-時雨おもらし本(2)",
    "主题类型":"转载",
    "网址":"https://www.shireyishunjian.com/main/forum.php?mod=viewthread&tid=298011&extra=page%3D1",
    "一级目录":"尿裤子|憋尿",
    "二级目录":"尿裤子|憋尿绘画区",
    "内容":[{
            "发帖人":"林偉傑",
            "发帖时间":"2025-5-11 19:46:41",
            "内容":"有興趣的可以拿去翻譯一下\n記得在分享回來這裡就好\n我也不知道為什麼被拆成兩篇文章\n圖片重用還是不能集中在一個帖子裡",
            "楼层":"1",
            "图片":["https://www.shireyishunjian.com/main/data/attachment/forum/202505/11/194508iy41e62jkocd6lts.jpg.thumb.jpg"]
    },
    {
        "发帖人":"金牛座金牛",
        "发帖时间":"2025-5-12 22:33:25",
        "内容":"感谢分享",
        "楼层":"2",
        "图片":[]
}
]
}
```

