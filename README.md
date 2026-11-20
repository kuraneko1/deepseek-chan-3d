# DeepSeek-chan 3D Viewer

**DeepSeek ちゃん（クジラメイド）** の 360° 回転対応・24 FPS 疑似 3D（スプライトスタッキング）インタラクティブビューワーです。  
単一 HTML ファイル（[`index.html`](./index.html)）に全 9 モーション × 24 フレーム（計 216 フレーム）・9 表情・3D ボクセル DeepSeek ロゴクジラ・海／水 3D パーティクル演出を完全内蔵しており、外部サーバーやインストール不要でブラウザからそのまま動かせます。

---

## プレビュー（GIF ギャラリー）

<table>
  <tr>
    <td align="center" width="33%">
      <img src="assets/gifs/demo_360.gif" alt="360° 回転ターンテーブル" width="260" /><br />
      <b>360° 回転（1. IDLE）</b><br />
      <sub>全角度シームレス WebGL 描画</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/gifs/demo_whale.gif" alt="DeepSeekロゴクジラとじゃれ合い" width="260" /><br />
      <b>7. WHALE（ロゴクジラとじゃれ合い）</b><br />
      <sub>3D クジラ前後 Z ソート＋ハート＆泡</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/gifs/demo_think.gif" alt="ジト目＋ムキムキCEO吹き出し" width="260" /><br />
      <b>6. THINK（CEO 吹き出しミーム）</b><br />
      <sub>無口ジト目＋頭上の CEO 吹き出し</sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="33%">
      <img src="assets/gifs/demo_shhh.gif" alt="CEOフレックス＆シーッ！ポーズ" width="260" /><br />
      <b>5. SHHH（CEO フレックス → シーッ！）</b><br />
      <sub>ドヤ顔＋指ポーズ＋キラキラ演出</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/gifs/demo_splash.gif" alt="ハイドロ三日月斬撃" width="260" /><br />
      <b>8. SPLASH（海洋攻撃①）</b><br />
      <sub>水色三日月斬撃＋3D 水しぶき＆水紋</sub>
    </td>
    <td align="center" width="33%">
      <img src="assets/gifs/demo_vortex.gif" alt="深海二重螺旋大渦巻き" width="260" /><br />
      <b>9. VORTEX（海洋攻撃②）</b><br />
      <sub>浮遊チャージ → 深海大渦巻き＋3重水紋</sub>
    </td>
  </tr>
</table>

<p align="center">
  <img src="assets/viewer_preview.png" alt="DeepSeek-chan 3D Viewer UI" width="820" />
</p>

---

## 簡単な使い方

### 開き方
1. このリポジトリをクローン、または [`index.html`](./index.html) をダウンロードします。
2. `index.html` を Chrome / Edge / Firefox / Safari などのモダンブラウザで開くだけです（`file://` 直開き対応・通信ゼロ）。

### 操作方法

| 操作 | 内容 |
| :--- | :--- |
| **左ドラッグ / スワイプ** | 360° 自由回転（自動回転を一時停止） |
| **マウスホイール** | ズームイン／アウト |
| **キーボード `1` 〜 `9`** | 全 9 モーション切替（`IDLE` / `WALK` / `HAPPY` / `WAVE` / `SHHH` / `THINK` / `WHALE` / `SPLASH` / `VORTEX`） |
| **`Space`** | アニメーション再生／一時停止 |
| **24-FRAME TIMELINE** | タイムラインをドラッグして好きな 1 コマで固定＆360° 回転鑑賞（水しぶき・渦巻きも静止観察可能） |
| **`F` キー / `FACE` ボタン** | 表情が見やすい顔アップ視点へ切替 |
| **`B` キー / `BOUNCE` ボタン** | 弾性バウンス（スクワッシュ＆ストレッチ） |
| **`Q` / `E` または `←` / `→`** | 左右へ連続回転 |
| **`R` キー / `RESET` ボタン** | 初期状態（`SQUASH 0.35` / `ICE LAB` / `SMOOTH AA`）へリセット |

### 主な表示カスタマイズ（右パネル）
- **RENDER STYLE**: `SMOOTH AA`（デフォルト）／`PIXEL+AA`（ピクセル粒感＋境界 AA）／`RETRO PX`（王道ドット絵）／`SILKY 3D`（フィギュア風滑らか）＋ `DOT SIZE` 調整
- **3D コントロール**: `ANIM FPS` (6〜36 FPS) / `SQUASH`（俯瞰角度 `0.35`〜`1.00`、`TOP` 真上視点） / `SPACING`（`SPREAD` で 160 スライス層を展開観察） / `ZOOM`
- **背景・演出**: `ICE LAB` / `DEEP SEA` / `MIDNIGHT` の 3 テーマ、`FX: ON/OFF`、`OUTLINE: ON/OFF`、`SPRING: ON/OFF`

---

## 使用している疑似 3D エンジン・スキル & クレジット

本作品の WebGL 2-Pass 描画エンジンおよびアニメ調 24 FPS 疑似 3D 制作手法は、キャラクター非依存の汎用スキル＆エンジンとして別リポジトリに分離・公開しています。

- **Anime Pseudo-3D Skill & Engine**: [kuraneko1/anime-pseudo-3d](https://github.com/kuraneko1/anime-pseudo-3d)
- **Credits & Inspiration**: 本作品のスプライトスタッキング（積層スライスによる疑似 3D ピクセルアート）の発想と基礎手法は、**[SpriteCook — Sprite stacking for fake 3D pixel art cars and props](https://www.spritecook.ai/blog/sprite-stacking-pixel-art)** から多大なる影響を受けています。また汎用基盤として [kuraneko1/sprite-stacking-3d](https://github.com/kuraneko1/sprite-stacking-3d) の知見を活用しています。

---

## License

[MIT License](./LICENSE)
