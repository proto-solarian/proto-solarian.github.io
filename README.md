# 光エンジン Hikari Engine
自製レンダリングAPIとゲームエンジン実験プロジェクト。暇な瞬間だけに開発して３か月に作成しました。
A rendering API and game engine research project. This project was buil over the course of 3 months while working a full time job.

## テクノロジー Technologies
プログラミング言語
Languages:
- C/C++
- Slang (HLSL)
利用ユーティリティライブラリー等
Utilities:
- Vulkan 1.3
- GLM
- 他に利用されておりません No other APIs, Libraries, or Frameworks were used

## エンジン機能 Engine Features
- Wavefront .OBJファイルインポーター Wavefront .OBJ file importer
- 三部構成 3-Part Architecture:
  - エンジンコア Engine Core
  - アプリ（エディターの基盤）App(Editor base)
  - 競合ライブラリー Shared library
- 構築可能なシーンオブジェクトヒエラルキー/トランスフォームツリー Scene object hierarchy/composable transform tree
- オブジェクトの行動をアプリ側でプログラム出来る Customizable object behaviors
- エンティティコンポーネントシステム（ECS）の形にメモリ領域を定義している（例えば、アプリ側で作成された行動オブジェクトは連続メモリに書き込み、アップデート関数はフレーム毎に連続に呼び出しています）
  Entity-Component System (ECS) consideration for memory locality (i.e.: customized behaviors exist in contiguous memory and their Updates are called sequentially)
- WindowsとAndroidに対応するように構築しています（現在Windowsのみに対応しています）Built with Windows and Android in mind, but currently only supports Windows

## レンダラー機能 Renderer Features
- プロメテウスという完全自製のVulkanレンダラー A completely bespoke vulkan-based renderer called Prometheus
- 単純な拡散反射シェーディング Simple, diffuse shading
- アプリ側で構築できるライティング App-side Lighting
- 最適化しているフレームアップデート構成　Highly performant frame updates

## 次に実装する予定のエンジン機能 Upcoming Engine Features (Short-term)
- イメージインポート（AVIFかwebpを調査する予定だが、DCCワークフローをサポートする為にTIFFにする可能性が高い） Image importing (AVIF or Webp possible, but TIFF to support artist workflows)
- 他の3Dモデルファイル形式をサポートする（FBX実装する可能性が高いが、理想的にGLTF/GLBをサポートしたい） More mesh importing (FBX likely, GLTF/GLB ideal)
- アンドロイド対応 Android support
- ユーザーインプット読み込み Input handling

## 次に実装する予定のレンダラー機能 Upcoming Renderer Features　（Short-term）
- テキスチャー利用するシェーディング Texturing
- PBRシェーディング PBR Shading
- スカイボックス Skyboxes
- 透明なオブジェクトの描画 Transparent object drawing
- グローバルイルミネーション Global illumination
- シャドーマップ Shadow mapping

## 後で実装する予定のエンジン機能 Upcoming Engine Features (Long-term)
- 仮想現実/空間レンダリングサポート Virtual Reality/Spatial Rendering Support
- シーンエディターインターフェース Scene editor interface

## 後で実装する予定のレンダラー機能 Upcoming Renderer Features (Long-term)
- 未決定（現代的・次世代のレンダリング機能の実装する方法を複数実験する予定）
