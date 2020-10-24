# 八週切版練習筆記

## W1_個人履歷[（設計稿）](https://xd.adobe.com/view/0f1c0abb-4063-4ed0-96b1-452f520f878b-5a4f/)
#### 個人學習註記
```
* box = width +border + padding

* 「行距」推擠成高度，預設就是 1倍 * font-size

* 圖片預設底下有 margin-bottom:2-3px
  1. 使用 display:block 修正
  2. 使用 vertical-align: middle 修正
  
* 不寫死寬度但又能設定 margin auto 的方法（類似 justify-content:center 的效果）
   https://developer.mozilla.org/en-US/docs/Web/CSS/fit-content
   
  .item-center{ 
   margin: 0 auto;
   max-width: fit-content（讓母元素寬度適應子元素）
   }
```

#### 作品修正
```
- 主要對直接在 html tag 上寫樣式這點進行修正，為元素進行添增 class
- class 採用 BEM 命名
- 將 css 區分為三類：基本設定 + utility樣式/ 基本區塊元件樣式/ 個別區塊樣式
```

- [x] 不建議寫死樣式在 HTML 標籤上，因為一個網站的頁面，會有很多個 h2 或 p 樣式，這樣在覆蓋樣式上會比較困難，可以設定 class
- [x] 建議 個人資料 、學歷 ... 內容最外層 div 可以命名 class 為 .profile 、 .edu ...這樣可以更清楚明瞭結構
- [x] h1 外層不需要再包一層 div，拿掉後可以讓結構更簡潔
- [x] 學歷、技能， li 內不需在包 p 標籤，寫在 li 上即可
- [ ] 工作經驗的 .container 也可以寫在 section 上，減少不必要的 div 使用
> [color=#DB4D6D] 希望保持架構的一致性，故不進行更動

- [x] 工作經驗內的標題名稱可使用 h3 標題標籤
- [x] footer 區塊 a 標籤連結加上 hover 效果，讓滑鼠滑入時有顏色變化，可以提升使用者體驗
- [x] footer「電話」的部分，讓使用者直接撥打電話體驗，可以使用
` <a href="tel:+886-910123456"> 0910-123-456 </a> `
- [x] 此份設計稿不需用到 flex 來設計，技能及聯絡方式 ul 設定寬度並使用 margin: 0 auto; 水平置中。.img-center 的 flex 刪除，可以在 .social-img 設定 display:inline-block;
> [color=#DB4D6D] `max-width: fit-content` 可以達成不設定寬度又能使用 margin:auto 的效果

---
## Week2
```
* 具固定寬度的容器與子元件，當子元件總寬度超過容器時，子元件會依照比理改變寬度自適應容器。
若希望子元素換行的話，使用 `flex-wrap:wrap`
```
https://codepen.io/irishuang/pen/yLJgqRe