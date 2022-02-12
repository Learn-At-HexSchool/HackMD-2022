# [LOG]_Week05-VUE-2022

###### tags: `real-time`
 
![](https://img.shields.io/badge/Created_Date-11_Feb_2022-orange)  [![hackmd-github-sync-badge](https://hackmd.io/iu6nrEPYRa-whG0ZUOrXgQ/badge)](/iu6nrEPYRa-whG0ZUOrXgQ?both)


:::info

- **【今日討論串】**

> 
> - https://discord.com/channels/801807326054055996/905656987583397908/941660614043000872
> 



:::



---

[TOC]

---

:::warning 
- **【預計 tag】**_可用 `F3` 快速搜尋
    - [ ] 待補充項目：==`#TODO`==
    - [ ] 建議練習的部分：==`#Practice`==
    
:::

---
---

## Summary

- 若資源跟不上
    - 請優先專注在主線任務就好

- 首波截止線：3 月 4 日
    - 剩 20 天

>
> - https://hackmd.io/@dbFY0UD9SUeKmNXhWf01ew/Hy63oE7y5#課程獎勵說明：
>

- 本次重點任務：
    - 作業的表單驗證
    - `Vue-CLI`

- 最終作品建議
    - 要可以像正式上線的網站
    - Lv.3 期限在 3/18
    - Wee07 會有設計講師
    - 後台不會檢核畫面

---

## [19:45]_Chat

- ==`#TODO`==

---

## [20:00]_開場

- 介紹加碼項目

---

### [20:15]_簡單講解作業

---

### [20:17]_課前小測驗-1

---

## [20:36]_PartI-`watch`

>
> - https://hackmd.io/@dbFY0UD9SUeKmNXhWf01ew/Hy63oE7y5#元件關聯進階方法
> 

- 情境：無法更動外層的資料
    - 需要在內層宣告新變數來接收（在生命週期初始化的時候）

- 但新狀況是：若外層資料跟著變動時
    - 要如何讓內層資料也可以連動？
    - 解法：`watch`
        - `watch` 可以監控 `props` 的變化

- #QA：`computed`？
    - `computed` 無法操作資料

---

### [20:45]_`$refs`

- 操作 `DOM` 元素

```=JS

this.$refs.div.innerHTML = "123"

```

- `ref` 的命名可以自訂

```=HTML

<card ref="myCard"></card>

```

- 可以進到元件

```=JS

console.log(this.$refs.myCard)

```

- 呼叫元件裡面的方法

```=JS

this.$refs.myCard.changeText()

```

---

### [20:54]_`ref`x`modal`

![](https://i.imgur.com/kx1hoRw.png)

- 好用方法

```=JS

this.$refs.callModal.openModal()

```

---

### [21:06]_`ref`x`watch`

![](https://i.imgur.com/o20DM93.png)

- 原因：只有在 `mounted()` 的時候傳送資料過去
    - 所以不會同步更新資料
    - 解法：`watch`

---

## [21:14]_跨元件溝通-`mitt`

>
> - https://hackmd.io/@dbFY0UD9SUeKmNXhWf01ew/Hy63oE7y5#Vue-外部插件
> 

![](https://media.discordapp.net/attachments/928115110478745664/941684382354247800/unknown.png)

- 沒有層級限制

- 過去的內建版本：`Event Bus`
    - 後來移除惹
    - 所以現在 `mitt` 是外部的擴充套件


>
> - https://github.com/developit/mitt#install
> 

- 新手教學-Step0
    - 匯入 CDN
    - 宣告 => 啟用函式

```=JS

<script src="https://unpkg.com/mitt/dist/mitt.umd.js"></script>

const emitter = mitt()


```

- Step1
    - 事件監聽

- Step2
    - 觸發事件



- `emitter`x`loding` -> 很適合放在生命週期裡面

- 地雷：打錯字不會噴錯

---

### [21:32]_小問題系列

- Q1
    - ==#TODO:==

- Q2

```=JS

emitter.emit('call-emit')

```

- Q3 

```=JS

emitter.on('call-emit', () => { } )

```

---

## [21:42]_外部元件_`loding-overlay`

- `Vue Loading Overlay Component`
> 
> - https://www.npmjs.com/package/vue-loading-overlay
>

### QK

## [21:59]_表單驗證

>
> - https://hackmd.io/@dbFY0UD9SUeKmNXhWf01ew/Hy63oE7y5#VeeValidation-知識點
>

- 驗證要寫規則

- `label for` <-> `input id`
    - `name` 傳給伺服器用的
    - `input type` 會影響使用者體驗

![](https://i.imgur.com/wyjpafg.png)


- 按鈕 -> `type=sumbit`
    - 會把整個表單事件送出去

---

### [22:12]_實作表單驗證

> - 【攻略手冊】
>   - https://hackmd.io/@hexschool/Hkg6N_Dbd
> 

- 像 `change` 的效果

- 自訂錯誤訊息：直接修改 `.json`

---

### [22:24]_下拉選單

---

### [22:25]_主線作業

- 可以參考攻略手冊跟著做

---

### [22:27]_團隊任務講解

- 必要：`Vue-CLI`

---

### [22:29]_獎勵再介紹


