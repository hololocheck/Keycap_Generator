# Keycap Generator

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-r160-00e5ff.svg)
![Version](https://img.shields.io/badge/version-67.0-orange.svg)

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

### 📝 アップデート情報 (V67.0)
**"Visual Mastery & Manufacturing" Update**
3D空間での直感操作と、製造品質を極めるための大型アップデートです。
- **ビジュアル・操作革命**: 「フローティングHUD」を一新。「ガムボール」による直感的なパーツ移動、「ビューキューブ」による視点切り替え、設定を瞬時に保存・復元できる「ギャラリー機能」を搭載。
- **エンジニアリング (CSK)**: 従来のランナー生成を進化させた「Custom Sprue Kit (CSK)」を実装。ギャラリーからD&Dで配置し、サイコロ型UI（Dice UI）で印刷向きを直感的に指定してキット化できます。
- **製造品質の向上**: 独自ライブラリ `MeshFixLib` による非多様体エッジの自動修復機能、および多種ステム（Alps / Kailh Choc / Topre）の生成に対応。
- **AMS完全連携**: Bambu Lab AMSに最適化されたカラーシステムを採用。スライサー画面のキャプチャによる色設定の取り込みや、3MFエクスポート時のカラー同期を実現しました。
- **システム改善**: レスポンシブUI対応、エクスポートボタンの統合、F5キーによるデバッグモードの実装。

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

### 📝 Update Notes (V67.0)
**"Visual Mastery & Manufacturing" Update**
A major update dedicated to mastering intuitive operation in 3D space and manufacturing quality.
- **Visual Revolution**: Revamped "Floating HUD". Features "Gumball" for intuitive part movement, "View Cube" for viewpoint switching, and "Gallery" to instantly save and restore settings via snapshots.
- **Engineering (CSK)**: Introduced "Custom Sprue Kit (CSK)". Create kits by Drag & Drop from the gallery, and intuitively set print orientation using the "Dice UI".
- **Manufacturing Quality**: Implemented automatic non-manifold edge repair via `MeshFixLib` and added support for diverse stem types (Alps / Kailh Choc / Topre).
- **Full AMS Integration**: Optimized color system for Bambu Lab AMS. Supports color setting import via slicer screen capture and full color synchronization during 3MF export.
- **System Improvements**: Responsive UI support, unified export button, and Debug Mode accessible via F5 key.

---

### 🛠 Technology Stack / 技術スタック
- **Engine**: [Three.js](https://threejs.org/)
- **Geometry Logic**: [three-bvh-csg](https://github.com/gkjohnson/three-bvh-csg), MeshFixLib(Custom)
- **Exporter**: STLExporter, OBJExporter, 3MFExporter(Original)

### 📄 License / ライセンス
MIT License.
