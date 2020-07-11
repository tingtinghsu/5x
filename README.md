# 5x
5x layout

切版實作紀錄

# `header`

Time: 30min

## Issue solved

### Question 1.

`.nav`bar靠齊右側

Solution：

一開始使用`margin left`發現調靠右太沒效率，後來想到可以使用`justify-content`

```html
.header {
  font-size: 0;
  justify-content: space-between; /*讓左右兩欄靠外*/
  box-sizing: border-box;  /* padding不超過1200px */
}
```



# footer

Time: 60min

## Issue solved

### Question 2.

footer的五倍logo無法對齊，會貼緊到左上側

Solution:

使用`align-items: center`

### Question 3.

讓footer的六欄項目全部靠上

Solution:

`align-items: flex-start`

```css
.footer {
  display: flex;
  align-items: center flex-start;  
  /* 要置中，不然會貼齊到左上方; ul li 對齊上方 */
  flex-wrap: wrap;
}
```



# Banner

Time: 5min

## Issue solved

### Question 4.

去掉空白問題，Banner下方有一條白白的線

Solution: `margin: 0px`

```css
.slide img {
  margin: 0px;    
}
```



# About

Time: 30min

### Question 5.

圖片分散對齊問題

Solution: `justify-content: space-around;`

```css
.container-about{
  width: 100%;
  text-align: center;
  display: flex;
  justify-content: space-around;
}
```

另外，隨著專案演進，我想讓about內的文字設定和下方的紅線可以被其他重複利用



# Recommand

Time: 90min

### Question 6.

avatar圖片和推薦文字分兩欄

Solution: `display flex`再設margin為auto

```css
.recommand-column {
  display: flex;
  /* 問題：無法分兩列 */
  width: 60%;
  margin: auto;
}
```



### Question 7.

此欄位的title想要引用之前`<div>`about的設定，但是因為about已設寬度`width: 1200px`，強加設定後此title會往左偏移

```css
.about {
  width: 1200px;
  color: #555555;          
  margin-top: 50px;
  text-align: center;
  font-size: 28px;
  font-weight: 400;
}
```

用註解比對發現是寬度的問題

```scss
.recommandation .about-course {
    text-align: center;
    color: #555555;  
    margin-top: 50px;
    margin-bottom: 50px;
    /* width: 1200px; */
    font-size: 28px;
    font-weight: 400;          
}
```

修了很久為了不想讓設定一直跑掉，決定暫時不要整理程式嗎