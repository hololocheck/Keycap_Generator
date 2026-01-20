# Keycap Generator

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Three.js](https://img.shields.io/badge/Three.js-r160-00e5ff.svg)
![Version](https://img.shields.io/badge/version-65.0-orange.svg)

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

### 📝 アップデート情報 (V65.0)
- **ビデオヒント機能**: パラメータにカーソルを合わせると、機能の効果を解説する短い**動画(Video/GIF)**がツールチップ内で自動再生されるようになりました。
- **X (Twitter) シェア**: 現在のデザイン設定を埋め込んだURLを、ワンクリックでXへ投稿・共有できるボタンを追加しました。
- **新テクスチャ追加**: 表面加工に「Ripple (波紋)」「Wood (木目)」「Hammered (打痕)」などの新パターンを追加しました。
- **バグ修正**: カスタムフォントを読み込んだ際、既存のプリセットフォントが選択できなくなる問題を修正しました。

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

### 📝 Update Notes (V65.0)
- **Video Hints**: Tooltips now include **Video/GIF** demonstrations that automatically play on hover, visually explaining parameter effects.
- **Share to X (Twitter)**: Added a button to instantly post and share your design URL to X with a single click.
- **New Textures**: Added new surface procedural patterns such as "Ripple", "Wood", and "Hammered".
- **Bug Fix**: Resolved an issue where loading a custom font would make existing preset fonts unavailable.

---

### 🛠 Technology Stack / 技術スタック
- **Engine**: [Three.js](https://threejs.org/)
- **Geometry Logic**: [three-bvh-csg](https://github.com/gkjohnson/three-bvh-csg)
- **Exporter**: STLExporter, OBJExporter, 3MFLoader(Customized)

### 📄 License / ライセンス
MIT License.
