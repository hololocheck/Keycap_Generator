# Keycap Generator

<p align="center">
  <img src="keycapgeneratorIcon.svg" width="120" alt="Keycap Generator">
</p>

<p align="center">
  <strong>Browser-based 3D Keycap Generator</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License">
  <img src="https://img.shields.io/badge/Three.js-r160-00e5ff.svg" alt="Three.js">
  <img src="https://img.shields.io/badge/version-68.1-orange.svg" alt="Version">
</p>

[日本語](#japanese) | [English](#english)

---

<a id="japanese"></a>
## 🇯🇵 日本語 (Japanese)

ブラウザ上で動作する、高機能な3Dキーキャップ・ジェネレーターです。主要なプロファイルに対応し、刻印からSTL/3MF書き出しまでシームレスに行えます。

### 🌐 関連リンク
- **[Keycap Generator Wiki](https://keycapgeneratorwiki.com/ja/home)**: 各種パラメータの詳細な解説、デザインのTips、トラブルシューティングを掲載しています。
- **[ツールページ](https://hololocheck.github.io/Keycap_Generator/)**: **インストール不要。** ブラウザから最新版を直接利用できます。
- **[Keycap Slicer Bridge](https://github.com/hololocheck/Keycap-Slicer-Bridge)**: BambuStudio / OrcaSlicer との連携ブリッジツール。

### 💡 インストール不要で即座に利用可能
このツールはクライアントサイドJavaScriptのみで構築されているため、ソフトウェアのダウンロードや複雑な環境構築は一切不要です。
- **Serverless**: 全ての演算（3D形状生成、CSG演算）がブラウザ上で完結します。
- **Cross-Platform**: Windows, Mac, Linuxなど、ブラウザがあれば即座に設計・エクスポートが可能です。

### ✨ 主な機能
- **多種多様なプロファイル**: Cherry, OEM, SA, XDA, DSAを搭載。
- **高度なテキスト編集**: 複数行印字、曲面への自動追従（Conform）、ダブルショット風書き出し。
- **SVGアイコン対応**: オリジナルロゴ（SVG形式）をキーキャップ表面に配置可能。
- **外部モデル合成 (Remix)**: 既存STLの結合（Union）や型抜き（Subtract）が可能。
- **3Dプリント最適化**: ステムのクリアランス調整、補強リブ、Lego Stud対応。
- **スライサー連携**: Keycap Slicer Bridge によるフィラメント同期＆3MFダイレクト転送。
- **コスト・重量計算**: フィラメントに応じた概算重量とコストをリアルタイム算出。

### 📝 アップデート情報 (V68.1)
**"Slicer Bridge" Update**

スライサーとの連携を大幅に強化するアップデートです。OrcaSlicer対応、フィラメント自動同期、24色AMS対応を実現しました。

- **OrcaSlicer フィラメント自動検出**: OrcaSlicer の `orca_presets` 配列構造を解析し、現在選択中のプリンターに対応するフィラメント色・名前を自動取得。3段階マッチング（完全一致→部分一致→最終エントリ）でプリンターを特定。
- **BambuStudio MD5修正**: `BambuStudio.conf` 末尾の MD5 チェックサム行によるJSONパースエラーを `raw_decode` 方式で解消。
- **24色対応**: AMS（16色）+ AMS HT（8色）= 最大24色。16色超過分はHTスロット（17–24番）に自動振り分け。
- **スプリットボタンUI**: AMS同期ボタンをエクスポートボタンと同じスプリットボタン方式に統一。テーマカラー（Bambu Studio＝緑 / OrcaSlicer＝ティール）で接続状態を視覚的に表示。
- **モバイル修正**: モバイル端末でのエクスポートボタン表示を修正（スプリットボタン非表示化）。
- **SVGマネージャー修正**: DOMParser の `removeAttribute` エラーに try-catch を追加。
- **UI整理**: 絵文字アイコン（🔄, ⚡）を除去、冗長なJSONインポート/エクスポートボタンを削除。

> **V68.0 ("Typography & Workflow") のハイライト:**
> * **3Dフォントエンジン**: FontEngine3D により .ttf/.otf/.woff フォントを直接読み込み。
> * **ターゲット別フォント**: メイン文字・サブ文字・サイド印字にそれぞれ異なるフォントを設定可能。
> * **フォントマネージャー / SVGマネージャー**: カスタムアセットの管理・永続化ダイアログ。
> * **環境バックアップ**: 全パラメータ・ギャラリー・フォント・SVG・AMS設定を1ファイルで一括保存。
> * **HUD拡張**: 配置モード、生成モード、寸法線ボタン追加。アクティブ状態でシアンに変色。
> * **エクスポート統一**: 全エクスポート処理を単一プログレスバー（%表示）に統一。

> **V67.0 ("Visual Mastery & Manufacturing") のハイライト:**
> * **ビジュアル革命**: フローティングHUD、ガムボール操作、ギャラリー機能の実装。
> * **エンジニアリング (CSK)**: ランナー枠付きキット生成機能と、ダイスUIによる直感的な向き指定。
> * **AMS完全連携**: スライサー同期と画面キャプチャによる色設定取り込み。
> * **製造品質**: 非多様体エッジの自動修復機能 (MeshFixLib) と多様なステム生成。

---

<a id="english"></a>
## 🇺🇸 English

A high-performance 3D keycap generator that runs in your browser. Supports major profiles and provides seamless workflow from design to STL/3MF export.

### 🌐 Related Resources
- **[Keycap Generator Wiki](https://keycapgeneratorwiki.com/ja/home)**: Comprehensive guide for parameters, design tips, and troubleshooting.
- **[Tool Page](https://hololocheck.github.io/Keycap_Generator/)**: **No installation required.** Access the latest version directly in your browser.
- **[Keycap Slicer Bridge](https://github.com/hololocheck/Keycap-Slicer-Bridge)**: Bridge tool for BambuStudio / OrcaSlicer integration.

### 💡 No Installation Required
Built entirely with client-side JavaScript, this tool requires no downloads or environment setup for both English and Japanese versions.
- **Serverless**: All 3D geometry generation and CSG operations are performed locally in your browser.
- **Cross-Platform**: Accessible from any PC (Windows, Mac, Linux) simply by visiting the link.

### ✨ Key Features
- **Various Profiles**: Pre-installed Cherry, OEM, SA, XDA, and DSA profiles.
- **Advanced Text Editing**: Multi-line legends, surface conforming, and double-shot style export.
- **SVG Icon Support**: Place your logos (SVG) directly on the keycap surface.
- **3D Model Remixing**: Import STL files for Union or Subtraction (Engraving) operations.
- **3D Print Optimization**: Stem clearance adjustment, reinforcement ribs, and Lego Stud support.
- **Slicer Integration**: Filament sync & direct 3MF transfer via Keycap Slicer Bridge.
- **Cost & Weight Calculation**: Real-time estimated weight and cost based on filament.

### 📝 Update Notes (V68.1)
**"Slicer Bridge" Update**

A major update that greatly enhances slicer integration. Adds OrcaSlicer support, automatic filament sync, and 24-color AMS support.

- **OrcaSlicer Filament Auto-Detection**: Parses OrcaSlicer's `orca_presets` array structure to automatically retrieve filament colors and names for the currently selected printer. 3-stage matching (exact → partial → last entry) identifies the correct printer.
- **BambuStudio MD5 Fix**: Resolved JSON parse error caused by the MD5 checksum line appended to `BambuStudio.conf` using the `raw_decode` method.
- **24-Color Support**: AMS (16 colors) + AMS HT (8 colors) = up to 24 colors. Colors exceeding 16 are automatically distributed to HT slots (17–24).
- **Split Button UI**: AMS sync button redesigned to match the export button's split button style. Theme color indication (Bambu Studio = green / OrcaSlicer = teal) shows connection status at a glance.
- **Mobile Fix**: Corrected export button display on mobile devices (split button artifacts removed).
- **SVG Manager Fix**: Added try-catch for `removeAttribute` DOMParser errors.
- **UI Cleanup**: Removed emoji icons (🔄, ⚡) and redundant JSON import/export buttons.

> **V68.0 ("Typography & Workflow") Highlights:**
> * **3D Font Engine**: FontEngine3D loads .ttf/.otf/.woff fonts directly — no conversion needed.
> * **Per-Target Fonts**: Set different fonts for Main Text, Sub Text, and Side Print.
> * **Font Manager / SVG Manager**: Dedicated dialogs for managing and persisting custom assets.
> * **Environment Backup**: Back up all parameters, gallery, fonts, SVGs, and AMS settings in a single file.
> * **HUD Enhancements**: Added Placement mode, Generation mode, Dimension buttons. Active toggles turn cyan.
> * **Export Unification**: All export operations unified to a single progress bar with percentage display.

> **V67.0 ("Visual Mastery & Manufacturing") Highlights:**
> * **Visual Revolution**: Floating HUD, Gumball operation, and Gallery features.
> * **Engineering (CSK)**: Custom Sprue Kit generation with intuitive "Dice UI" for orientation.
> * **Full AMS Integration**: Slicer synchronization and color setting import via screen capture.
> * **Manufacturing Quality**: Automatic non-manifold edge repair (MeshFixLib) and diverse stem generation.

---

### 🛠 Technology Stack / 技術スタック
- **Engine**: [Three.js](https://threejs.org/)
- **Font Engine**: FontEngine3D (Custom) — TTF/OTF/CFF/CFF2/WOFF
- **Geometry Logic**: [three-bvh-csg](https://github.com/gkjohnson/three-bvh-csg), MeshFixLib (Custom)
- **Exporter**: STLExporter, OBJExporter, 3MFExporter (Original)
- **Slicer Bridge**: [Keycap Slicer Bridge](https://github.com/hololocheck/Keycap-Slicer-Bridge) — BambuStudio / OrcaSlicer filament sync & direct transfer (v2.6.2)

### 📄 License / ライセンス
MIT License.
