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

```html
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

Solution:

```html
.slide img {
  margin: 0px;    
}
```

