# 5x
5x layout

切版實作紀錄

# `header`

Time: 30min

## Issue solved

Question 1.

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

