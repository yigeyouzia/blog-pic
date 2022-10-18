# blog-pic
---
title: 我的第一篇博客.md
date: 2022-10-17 18:36:44
tags:
- 第一篇
- 测试
categories:
- 一级分类
- 二级分类
---

# 一级标题

代码测试：

```py
print("Hello")
```

注意：这里因为我放在md文件中的，所以加上了\，不解析```，实际测试时请去掉\。

图片测试：

![](http://mculover666.cn/blog/20191031/R4mWMXsrRKxu.png?imageslim)

引用测试：

>这是一条引用

## 二级标题

无序列表测试：

- 哈哈
- 嘿嘿
- 吼吼

### 三级标题

#### 四级标题

## ![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662643872003-11194f3e-1093-49c3-ab95-39f65cdbb4bb.png)

![image.png](https://qpic.y.qq.com/music_cover/UROl51JnIAk9Ipxmv4b86p2XypfBWg9b4Iye05cvocqqRGerh6nhyA/300?n=1https://qpic.y.qq.com/music_cover/UROl51JnIAk9Ipxmv4b86p2XypfBWg9b4Iye05cvocqqRGerh6nhyA/300?n=1)

<a name="sAawY"></a>

## ![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662643872003-11194f3e-1093-49c3-ab95-39f65cdbb4bb.png)

<a name="rOKQs"></a>

## 3.1dropdown 下拉

<a name="JzfgP"></a>

### ==布局思路==
![](2022-10-18-19-26-31.png)

1.上面 全部商品分类 和下面列表应该在一个dropdown  div里面 宽度一样   命名：上面dt 下面dd<br />2.下拉菜单用列表  ul>li 来做   大盒子dd给定宽高背景 红色<br />3.li设置左margin：2px   里面文字有一定距离  pdding-left：10px   文字居中<br />4.hover做法  碰到li变色<br />5.后面箭头用after做

```html
<div class="dropdown">
  <div class="dt">全部商品分类</div>
  <div class="dd">
    <ul>
      <li>家用电器</li>
      <li>手机、数码、通信</li>
      <li>电脑、办公</li>
      <li>家居、家具、家装、厨具</li>
      <li>男装、女装、童装、内衣</li>
      <li>个户化妆、清洁用品、宠物</li>
      <li>鞋靴、箱包、珠宝、奢侈品</li>
      <li>运动户外、钟表</li>
      <li>汽车、汽车用品</li>
      <li>母婴、玩具乐器</li>
      <li>食品、酒类、生鲜、特产</li>
      <li>医药保健</li>
      <li>图书、音像、电子书</li>
      <li>彩票、旅行、充值、票务</li>
      <li>理财、众筹、白条、保险</li>
    </ul>
  </div>
</div>
```

<a name="GBvOx"></a>

### 小li做法

1.marfin-left 2px  为了点以后左边留红  美观

```css
.dropdown .dd ul li {
    position: relative;
    margin-left: 2px;
    height: 31px;
    line-height: 31px;
    padding-left: 10px;
    color: #fff;
}
```

<a name="FvrIy"></a>

###

<a name="JpINb"></a>

### 箭头做法  伪元素

1、用绝对定位 absolute<br />2.相对于父亲是li  li加相对定位relarive

```css
.dropdown .dd ul li::after {
  position: absolute;
  top: 1px;
  right: 10px;
  font-family: 'icomoon';
  content: '\e920';
  font-size: 14px;
}
```

<a name="ov6MZ"></a>

## 3.2navitems

![image.png](2022-10-17-19-38-54.png)

做法思路： 为了增大链接选项

1.设置ul  左浮动

2.**ul里放a   a为行内元素  给a转为inline-block     给padding撑开a的范围（左右距离各一半25）  用户鼠标放在盒子上有链接**

```css
.navitems ul li a {
    display: block;
    padding: 0 25px;
    line-height: 45px;
    font-size: 16px;
    font-weight: 500;
}
```


## ![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662643872003-11194f3e-1093-49c3-ab95-39f65cdbb4bb.png#clientId=uee011274-b7c1-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=597&id=Wje2N&margin=%5Bobject%20Object%5D&name=image.png&originHeight=746&originWidth=1765&originalType=binary&ratio=1&rotation=0&showTitle=false&size=46113&status=done&style=none&taskId=u4306080c-4fc0-4abe-8cdd-43aa53c3c63&title=&width=1412)

## 3.1dropdown 下拉

### 布局思路

1. 上面 全部商品分类 和下面列表应该在一个dropdown  div里面 宽度一样   命名：上面dt 下面dd
2. 下拉菜单用列表  ul>li 来做   大盒子dd给定宽高背景 红色
3. li设置左margin：2px   里面文字有一定距离  pdding-left：10px   文字居中
4. hover做法  碰到li变色
5. 后面箭头用after做

![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662643988840-a0cd0868-4745-4edd-90fc-2e9a84f72b32.png#clientId=u7d0a092e-9495-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=98&id=uf7333ba0&margin=%5Bobject%20Object%5D&name=image.png&originHeight=122&originWidth=1521&originalType=binary&ratio=1&rotation=0&showTitle=false&size=23090&status=done&style=none&taskId=u2ef45e4e-add0-45f6-9039-ae7c9476c3a&title=&width=1216.8)

## 布局

1.四个盒子div  左1  中2 右1

```html
<header class="header w">
        <div class="logo">
            <h1>
                <a href="index.html">品优购商城</a>
            </h1>
        </div>
        <div class="search">2</div>
        <div class="hotwords">3</div>
        <div class="shopcar">4</div>
    </header>
```

## logo

### ESO提权  logo做法

![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662645364111-80bc99c9-4199-439b-8640-68785ff3eca8.png#clientId=u2c9b84be-5397-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=486&id=u0903cfb5&margin=%5Bobject%20Object%5D&name=image.png&originHeight=607&originWidth=1328&originalType=binary&ratio=1&rotation=0&showTitle=false&size=355801&status=done&style=none&taskId=ue8920600-afa8-452b-873d-525c6779a4b&title=&width=1062.4)

```css
.header .logo {
    position: absolute;
    width: 171px;
    height: 61px;
    left: 0;
    top: 27px;
}


header .logo a {
    display: block;
    width: 171px;
    height: 61px;
    background: url(../images/logo.png) no-repeat;
    /* 隐藏文字 */
    font-size: 0;
    /* text-indent: -9999px;
    overflow: hidden; */
}
```

1.注意隐藏文字两种方式  `font-size: 0;`

2.插入logo的图片大小=div大小

---

## 搜素框做法

![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662645694469-73243e67-1ddf-46ae-bab9-84399c479b96.png#clientId=u2c9b84be-5397-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=48&id=u431c77aa&margin=%5Bobject%20Object%5D&name=image.png&originHeight=60&originWidth=712&originalType=binary&ratio=1&rotation=0&showTitle=false&size=1917&status=done&style=none&taskId=udddb188a-411b-44fc-ac89-86d994ad9dd&title=&width=569.6)
```html
<div _class_="search">
            <input_type_="search"_name_=""_**id**_=""_placeholder_="语言开发">
            <button>搜索</button>
</div>
```
### 大盒子
1.大盒子定位到中间  然后边框2  红色
**注释：input和buttom都是块级元素 加左浮动**
   border: 2pxsolid   **#b1191a**;
### intput
2.input  行内块元素  宽高量里面  
3.文字placeholder  设置pdding  10px
### buttom
4.文字白色  大小16px  背景红色

## 热词hotwords

![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662646299056-9a7072e4-06e0-4ff6-9432-ff6854564e16.png#clientId=u2c9b84be-5397-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=23&id=u770faa20&margin=%5Bobject%20Object%5D&name=image.png&originHeight=29&originWidth=564&originalType=binary&ratio=1&rotation=0&showTitle=false&size=4943&status=done&style=shadow&taskId=uf1a19706-64a6-419e-aee6-eac123f9d7f&title=&width=451.2)
**小链接直接用多个a标签  加上absolute绝对定位  left  top 定位**
_.header.hotwords_ {
    position: absolute;
    left: 346px;
    top: 66px;
}

---

## 购物车shopcar

![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662646368874-e167175e-7efe-4077-82ea-76a2f20cbce0.png#clientId=u2c9b84be-5397-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=60&id=u8dbb2b05&margin=%5Bobject%20Object%5D&name=image.png&originHeight=75&originWidth=232&originalType=binary&ratio=1&rotation=0&showTitle=false&size=2598&status=done&style=shadow&taskId=u038a946e-98aa-4fbc-b617-48bdfb05061&title=&width=185.6)

### 定位

绝对定位到位置   里面文字居中对齐
text-align: center;
    line-height: 35px;

### 前面小车

用before做,margin-right调整位置

```css
.shopcar::before {
    font-family: 'icomoon';
    content: '\e93a';
    color: #b1191a;
    margin-right: 5px;
}
```

### 后面箭头

margin-left调整位置

### 数字count 8

![image.png](https://cdn.nlark.com/yuque/0/2022/png/32698411/1662644034355-a4f06106-0fc5-4100-8de1-0022ba099f5e.png#clientId=u7d0a092e-9495-4&crop=0&crop=0&crop=1&crop=1&from=paste&height=198&id=ufc9cb5e9&margin=%5Bobject%20Object%5D&name=image.png&originHeight=248&originWidth=1120&originalType=binary&ratio=1&rotation=0&showTitle=false&size=83516&status=done&style=none&taskId=ud672de08-64fc-4392-a467-27c5229fa78&title=&width=896)
**count 给绝对定位：  行内元素i（类似span）   根据内容给大小**

```css
.count {
    position: absolute;
    left: 105px;
    top: -5px;
    right: 20px;
    /* 防止继承 */
    line-height: 14px;
    height: 14px;
    color: #fff;
    background-color: #c81623;
    padding: 0 5px;
    border-radius: 7px 7px 7px 0;
}
```
