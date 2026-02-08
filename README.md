# Keycap Generator

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-r160-00e5ff.svg)
![Version](https://img.shields.io/badge/version-67.1-orange.svg)

[日本語](#japanese) | [English](#english)

---

<a id="japanese"></a>
## 🇯🇵 日本語 (Japanese)

ブラウザ上で動作する、高機能な3Dキーキャップ・ジェネレーターです。主要なプロファイルに対応し、刻印からSTL/3MF書き出しまでシームレスに行えます。

### 🌐 関連リンク
- **[Keycap Generator Wiki](https://keycapgeneratorwiki.com/ja/home)**: 各種パラメータの詳細な解説、デザインのTips、トラブルシューティングを掲載しています。
- **[ツールページ](https://hololocheck.github.io/Keycap_Generator/)**: **インストール不要。** ブラウザから最新版を直接利用できます。

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
- **コスト・重量計算**: フィラメントに応じた概算重量とコストをリアルタイム算出。

### 📝 アップデート情報 (V67.1)
**"Mobile & Interaction" Update**

v67.0で実装された大規模機能を、より快適に利用するための改善アップデートです。

- **モバイル最適化**: スマートフォンからのアクセス時に、画面サイズに合わせてUIレイアウトが自動的に最適化されるようになりました。
- **操作性の向上**:
    - **スロット間ドラッグ**: AMSの色設定やCSKグリッド間で、アイテムをドラッグ＆ドロップして移動・入れ替えが可能になりました。
    - **UI視認性**: ショートカットパネルの「閉じる」ボタンの文字色を黒（#000）に変更し、視認性を改善しました。
    - **ドロップ制御**: 内部ドラッグ操作時に、外部ファイル読み込み用のオーバーレイが表示されないよう修正しました。
- **システム可視化**: メッシュ修復エンジンのロード状況を、詳細な4段階のプログレスバーで表示するように変更しました。

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
- **[ToolPage](https://hololocheck.github.io/Keycap_Generator/)**: **No installation required.** Access the latest version directly in your browser.

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

### 📝 Update Notes (V67.1)
**"Mobile & Interaction" Update**

An improvement update focusing on usability and smoother interaction based on v67.0 features.

- **Mobile Optimization**: Automatically optimized UI layout for smartphone access.
- **Interaction Improvements**:
    - **Drag & Drop**: Enabled item movement between AMS color slots and CSK grids via drag-and-drop.
    - **UI Visibility**: Changed the text color of the "Close" button to black (#000) for better contrast.
    - **Drop Control**: Suppressed the external file import overlay during internal drag operations.
- **System Visualization**: Replaced the loading indicator for the Mesh Repair Engine with a detailed 4-stage progress bar.

> **V67.0 ("Visual Mastery & Manufacturing") Highlights:**
> * **Visual Revolution**: Floating HUD, Gumball operation, and Gallery features.
> * **Engineering (CSK)**: Custom Sprue Kit generation with intuitive "Dice UI" for orientation.
> * **Full AMS Integration**: Slicer synchronization and color setting import via screen capture.
> * **Manufacturing Quality**: Automatic non-manifold edge repair (MeshFixLib) and diverse stem generation.

---

### 🛠 Technology Stack / 技術スタック
- **Engine**: [Three.js](https://threejs.org/)
- **Geometry Logic**: [three-bvh-csg](https://github.com/gkjohnson/three-bvh-csg), MeshFixLib(Custom)
- **Exporter**: STLExporter, OBJExporter, 3MFExporter(Original)

### 📄 License / ライセンス
MIT License.
