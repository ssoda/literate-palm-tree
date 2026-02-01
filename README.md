# 🎸 Web Guitar Tuner

一個使用 YIN 演算法的網頁吉他調音器，具有現代化的 Liquid Glass 視覺設計。

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ 功能特色

- **YIN 音高偵測演算法** - 高精度的音高偵測，適用於吉他調音
- **即時視覺回饋** - 動態調音指示器顯示音高偏差
- **標準吉他調音** - 支援 E2、A2、D3、G3、B3、E4 六弦
- **顏色編碼狀態**
  - 🟢 綠色 - 音準正確（±5 cents 內）
  - 🟡 黃色 - 偏高 (Sharp)
  - 🔵 藍色 - 偏低 (Flat)
- **響應式設計** - 支援桌面與行動裝置
- **Liquid Glass UI** - 現代化毛玻璃視覺效果

## 🚀 快速開始

### 使用方式

1. 直接在瀏覽器中開啟 `index.html`
2. 點擊 **Start Tuning** 按鈕
3. 允許瀏覽器存取麥克風
4. 彈奏吉他弦，調音器會自動偵測音高

### 線上使用

無需安裝，只需將檔案放置於任何 Web 伺服器即可使用。

## 🎯 技術實作

### YIN 演算法

本專案使用 YIN 音高偵測演算法，主要步驟包括：

1. **差分函數 (Difference Function)** - 計算信號自相關
2. **累積平均正規化差分 (CMND)** - 正規化差分值
3. **絕對閾值 (Absolute Threshold)** - 找出最小值點
4. **拋物線內插 (Parabolic Interpolation)** - 提高精度

### Web Audio API

使用瀏覽器原生的 Web Audio API 進行：
- 麥克風音訊擷取
- 即時音訊分析
- 頻率計算

## 📁 專案結構

```
tuner/
└── index.html    # 主程式（包含 HTML、CSS、JavaScript）
```

## 🌐 瀏覽器支援

| 瀏覽器 | 支援狀態 |
|--------|----------|
| Chrome | ✅ 完整支援 |
| Firefox | ✅ 完整支援 |
| Safari | ✅ 完整支援 |
| Edge | ✅ 完整支援 |

> ⚠️ 需要 HTTPS 或 localhost 環境才能存取麥克風

## 🎨 UI 設計

採用 **Liquid Glass** 設計風格：

- 動態漸層背景動畫
- 浮動模糊光暈效果
- 毛玻璃卡片 (`backdrop-filter: blur`)
- 玻璃反射與陰影效果
- 流暢的過渡動畫

## 📝 授權條款

本專案採用 MIT 授權條款。

## 🤝 貢獻

歡迎提交 Issue 或 Pull Request！
