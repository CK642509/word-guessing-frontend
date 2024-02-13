# Word Guessing Game Frontend
## Vue3 + TypeScript + Vuetify + PWA
## 簡介
### 說明
這是一個簡易猜單字的遊戲

### 規則
玩家開始遊戲後，將手機放置於自己的額頭上，讓其他玩家可以看到畫面中的單字/詞，而自己並不能看到自己的手機畫面。

透過玩家間的互動 (細節待補)，玩家需要努力猜測自己頭上的單字/詞是什麼，猜對後，點擊畫面左半邊即可加一分；反之，若選擇放棄，可以點擊右半邊。

### 安裝遊戲
> 建議使用手機等行動裝置進行遊玩

1. 進入[網站](https://vercel.com/ck642509/word-guessing-frontend)
2. 安裝遊戲到主畫面
3. 安裝完畢後，點擊應用程式進入遊戲

> 不安裝一樣可以遊玩，但會被瀏覽器的介面佔去許多畫面空間，進而降低遊戲體驗


## 開發
### 1. 安裝套件
```
npm install
```

### 2. 進入開發模式
```
npm run dev
```


## 建立各式 ICON
### 安裝套件
```
npm install -D vue-pwa-asset-generator
```

### 建立 icon
```
npx vue-pwa-asset-generator -a ./public/Teemo.png -o ./public/img/icons
```