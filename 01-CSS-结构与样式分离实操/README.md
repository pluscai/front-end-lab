# 一、什么是结构与表现分离？
> Html、CSS、Javascript分别代表了结构、写代码时，我们强调表现和行为，结构、表现、行为三者分离原则，什么才是真正的分离呢思想呢？

![图片](https://uploader.shimo.im/f/kif4VHn8OzYG3GVI.png!thumbnail)

如果把网页制作比作建造一座房子，html就是房子的结构、CSS就是后期的装修；所以在编写网页时，我们应该先从结构出发，做到html结构的合理简洁，在这种结构之上再进行CSS的设置，这样才能做到真正的表现与结构分离。
![图片](https://uploader.shimo.im/f/Pp5hdsKeu0MYb3oO.png!thumbnail)

那么当我们拿到一张效果图，应该怎么分析html结构和CSS样式呢。原则就是：
> 先不要过多的被样式打扰，重点放在HTML结构和语义化上
![图片](https://uploader.shimo.im/f/H1hbjkTbPqM0NFLf.png!thumbnail)
# 二、根据案例体会结构与表现分离思想
 微博用户发言信息列表的制作
仿腾讯微博，共同特点：左边是头像，右边是用户名字和发言内容
![图片](https://uploader.shimo.im/f/fLtxsicY6N8Iy4zL.png!thumbnail)

根据对结构和表现分离的理解的深度不同，有不同的思路和制作方法。
1、先考虑HTML结构和语义化，逻辑上，这个结构的组成可分为：头像、姓名、内容、发布时间，四个部分。
比较一下3个html结构，demo3的结构简洁、语义化呢
```
<!---demo01----------------------------------->
<div class="demo01">
  <div class="left">
    <img class="userPic" src="" width="50" height="50" />
  </div>
  <div class="right">
    <span class="pubTime">10分钟前</span>
    <h6>樱桃小丸子</h6>
    <p>奥鹏教育是由教育部高等教育司2001年12月批准立项试点</p>
  </div>
</div>

<!---demo02----------------------------------->
<div class="demo02">
  <img class="userPic" src="" width="50" height="50" />
  <div class="right">
    <span class="pubTime">10分钟前</span>
    <h6>樱桃小丸子</h6>
    <p>奥鹏教育是由教育部高等教育司2001年12月批准立项试点</p>
  </div>
</div>

<!---demo03----------------------------------->    
<div class="demo03">
  <img class="userPic" src="" width="50" height="50" />
  <h5>樱桃小丸子</h5>
  <p>奥鹏教育是由教育部高等教育司2001年12月批准立项试点</p>
  <span class="pubTime">10分钟前</span>
</div>
```
2、然后再写css，完整demo:
[https://jsfiddle.net/caishuxiang/ng8oe4k2/](https://jsfiddle.net/caishuxiang/ng8oe4k2/)
# 三、编程实操
![图片](https://uploader.shimo.im/f/kt7a7xqVKBQ97eVO.png!thumbnail)

用下面的代码进行修改，在线挑战地址：https://jsfiddle.net/caishuxiang/b846uy2c/

```
<style type="text/css">
body{ margin:0;}
div{background:#460E29;width:700px;padding:20px}
img{background:url(http://img.mukewang.com/5385ac820001905201440133.jpg)}
</style>
</head>
<body>
<div>
  <img src="http://img.mukewang.com/5385acb000013b0d00950095.jpg" />         
  <img src="http://img.mukewang.com/5385acb000013b0d00950095.jpg" />
  <img src="http://img.mukewang.com/5385acb000013b0d00950095.jpg" />
  <img src="http://img.mukewang.com/5385acb000013b0d00950095.jpg" /> 
</div>
</body>
</html>
```

