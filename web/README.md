# 公雞布偶 3D 網頁展示器

## 使用方式

1. 在專案根目錄啟動本機伺服器：`python3 -m http.server 8765`
2. 開啟 `http://127.0.0.1:8765/web/index.html`
3. 頁面會自動載入 `models/rooster-web.glb`（網站用壓縮版）。
4. 使用滑鼠拖曳旋轉、滾輪縮放，或按正面／側面／背面切換視角。
5. 也可用「選擇其他 GLB / glTF 檔案」載入其他模型。

## 尺寸校正

頁面載入後會以模型 Y 軸高度自動等比例校正為 18 cm，並顯示校正後的寬、高、深。原始設計圖標示約高 18 cm、正面寬 15 cm；Meshy 生成模型的比例仍需在 Blender 等 3D 軟體確認後才能打樣。

## 檔案說明

- `models/rooster.glb`：Meshy 原始 GLB（129 MB，Git LFS）
- `models/rooster-web.glb`：Draco + WebP 壓縮版（約 3.4 MB，普通 Git，供 Pages 使用）
- `models/rooster.stl`、`models/rooster.dxf`：原始高精度檔（Git LFS）
- `web/`：展示頁
- `images/`、`screenshots/`：預覽與視角截圖

## 部署

網站以專案根目錄為 GitHub Pages 來源，入口為 `/web/`。首次載入 Google model-viewer 元件需要網路連線。
