# p2p-doc-editor-proto

## 何を作りたい

- Markdown のリアルタイム共同編集機能を作りたい
  - 委員会で Growi を運用しているが、共同編集機能を作るには HackMD の設定が必要
  - HackMD のクレデンシャル周りがめんどくさいのと、できるだけ運用プロセスを増やしたくない
  - 共同編集機能だけ独立させた、**HackMD 統合と互換性のある静的アプリケーション**を作りたい
    - ただし、WebSocket サーバーを建てたくない
  - WebRTC で1人のユーザーがホストとなれば良さそう
  - Confluence 的な感じで編集者の誰でも現状を保存できる仕組みに

## 要件

- WebRTC を用いて Markdown の編集状況を共有できる
  - 「あいことば」を用いてピアに接続できる
- Markdown のリアルタイムプレビューを閲覧できる
- 静的アプリケーションである

## 使うもの

- React + Vite
- [yjs](https://www.npmjs.com/package/yjs)
- [y-webrtc](https://www.npmjs.com/package/y-webrtc)
- [@monaco-editor/react](https://www.npmjs.com/package/@monaco-editor/react)
- [y-monaco](https://github.com/yjs/y-monaco)
