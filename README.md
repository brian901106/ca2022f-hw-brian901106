# 電腦動畫 111-1 作業作品集

國立臺北科技大學「電腦動畫」課程（111 學年度第 1 學期）的作業作品集。主題是做出 Vtuber 需要的技術：前半學期用 Live2D 在網頁上做臉部追蹤，後半學期用 Unity 處理 3D 角色（VRM、MMD）和 Live2D。

**作品集網站：** https://brian901106.github.io/ca2022f-hw-brian901106/

## 作業一覽

| 作業 | 主題 | 說明頁 | 線上 Demo | 影片 |
|---|---|---|---|---|
| HW01 | Cubism Web SDK 發佈 Live2D | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw01/) | [Demo](https://brian901106.github.io/ca2022f-hw-brian901106/hw01/src/) | [YouTube](https://www.youtube.com/watch?v=_11Gf8Fm4NI) |
| HW02 | Live2D 展示頁（移動、縮放、換背景） | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw02/) | [Demo](https://brian901106.github.io/ca2022f-hw-brian901106/hw02/src/) | [YouTube](https://www.youtube.com/watch?v=gwA0_lZ6xJY) |
| HW03 | Slider 控制模型參數、觸碰發聲 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw03/) | [Demo](https://brian901106.github.io/ca2022f-hw-brian901106/hw03/src/) | [YouTube](https://www.youtube.com/watch?v=4utAHZmeLok) |
| HW04 | Face Landmarks Detection 網頁部署 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw04/) | [Demo](https://brian901106.github.io/ca2022f-hw-brian901106/hw04/src/) | [YouTube](https://www.youtube.com/watch?v=id46uL_Yzsk) |
| HW05 | 臉部特徵點驅動 Live2D 角色 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw05/) | [Demo](https://brian901106.github.io/ca2022f-hw-brian901106/hw05/src/) | [YouTube](https://www.youtube.com/watch?v=lX7O4dP1Rkk) |
| HW06 | MediaPipe + Live2D + OBS 直播 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw06/) | [Demo](https://brian901106.github.io/ca2022f-hw-brian901106/hw06/src/) | [YouTube](https://www.youtube.com/watch?v=GYcZCGL6EN4) |
| HW07 | VRoid 製作 VRM 角色並匯入 Unity | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw07/) | — | [YouTube](https://www.youtube.com/watch?v=W1nI3uY2ywg) |
| HW08 | Unity 角色多動作切換 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw08/) | — | [YouTube](https://www.youtube.com/watch?v=xAUbHKVM2ZU) |
| HW09 | MMD 模型（PMX → FBX）匯入 Unity | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw09/) | — | [YouTube](https://www.youtube.com/watch?v=gpFZ-jGTM6s) |
| HW10 | MMD 角色跳舞 + Timeline 運鏡錄影 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw10/) | — | [YouTube](https://www.youtube.com/watch?v=8Dd3QiclpU8) |
| HW11 | Cubism Unity SDK：視線跟隨、自動眨眼 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw11/) | — | [YouTube](https://www.youtube.com/watch?v=Qh25tLj9t50) |
| HW12 | Unity Live2D 動畫輪播、麥克風對嘴、透明背景執行檔 | [連結](https://brian901106.github.io/ca2022f-hw-brian901106/hw12/) | — | [YouTube](https://www.youtube.com/watch?v=lKF8Jb1ugGs) |

> 網頁 Demo 大多需要滑鼠操作；HW04–HW06 會用到攝影機，請用桌機版 Chrome / Edge 開啟並允許攝影機權限。

## 各作業內容

### Part 1：Live2D × 網頁

- **HW01**：下載並編譯 Cubism Web Samples，把 Live2D 模型換成 hijiki 後發佈成網頁，角色視線會跟著滑鼠。
- **HW02**：用 Haru 模型做 Live2D 展示頁，角色可以上下左右移動、縮放，拖曳圖片就能換背景。這份作業也學了怎麼透過 `window.update` 從 JS 呼叫 TypeScript 的功能。
- **HW03**：用 Slider Bar 綁定 AngleX/Y/Z、眉毛（BrowLY、BrowRY、BrowLX、BrowRX）等標準參數，點到角色身體會播放聲音。
- **HW04**：編譯 TensorFlow.js [Face Landmarks Detection](https://github.com/tensorflow/tfjs-models/tree/master/face-landmarks-detection) 並部署成網頁，可以即時偵測攝影機畫面，也能分析上傳的影片。
- **HW05**：把 HW04 抓到的臉部特徵點接到 Cubism 角色參數上，可以控制眉毛、左右擺頭、上下點頭、眨眼、歪頭、嘴巴開合，等於在網頁上做出自己的 FaceRig。
- **HW06**：用 MediaPipe Face Mesh 加上 One Euro Filter 平滑化來驅動 Live2D，再透過 OBS Studio 串流到 YouTube 直播。

### Part 2：3D 角色 × Unity

- **HW07**：用 VRoid Studio 做一個 VRM 角色（以同學為原型），匯入 Unity 讓角色動起來，並套用 Booth 買的衣服材質。
- **HW08**：在 Unity 裡讓 VRM 角色切換三個以上的動作（跳舞、走路等）。附 `hw08.unitypackage` 和示範影片。
- **HW09**：用 MMD4Mecanim 把 MMD 模型從 PMX 轉成 FBX 後匯入 Unity，另外也轉了其他 MMD 模型。
- **HW10**：讓 MMD 角色在 Unity 場景裡跳舞，用 Timeline 設定多個分鏡和軌道攝影機繞圈運鏡，最後用 Unity Recorder 錄成影片。

### Part 3：Live2D × Unity

- **HW11**：安裝 Cubism Unity SDK 並匯入 Live2D 模型，角色視線跟著滑鼠，另外寫腳本讓角色定時眨眼。
- **HW12**：角色會輪播三個以上的動畫，可以用麥克風控制嘴巴，最後把背景改成透明並 build 成執行檔。

## 目錄結構

```
.
├── index.html        # 導向 hw00 作品集首頁
├── hw00/             # 作品集首頁（頭像、各作業入口）
├── hw01 ~ hw06/      # 網頁作業：index.html 為說明頁，src/ 為可執行的 Demo
├── hw07 ~ hw12/      # Unity 作業：說明頁、截圖、影片、unitypackage
└── hw13 ~ hw18/      # 預留（尚未使用）
```

每份作業的 `index.html` 都有該次作業的心得、評分項目和 Demo 影片。

## 本機執行

網頁 Demo 需要透過 HTTP server 開啟（直接雙擊 HTML 會因為瀏覽器安全限制載入失敗）：

```bash
python -m http.server 8000
```

然後打開瀏覽器，前往 http://localhost:8000。

## 使用技術

- **Live2D**：Cubism SDK for Web、Cubism SDK for Unity
- **臉部追蹤**：TensorFlow.js Face Landmarks Detection、MediaPipe Face Mesh
- **3D**：VRoid Studio、UniVRM、MMD4Mecanim、Unity Timeline / Recorder
- **直播**：OBS Studio、YouTube Live
- **前端**：TypeScript、JavaScript、Bootstrap、dat.GUI

## 授權說明

Live2D 範例模型、MMD 模型、Booth 衣服素材等第三方素材的著作權屬於原作者，只用於課程學習。
