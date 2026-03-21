# TODO アプリ プロジェクト振り返り

## 📊 プロジェクト概要

- 期間: 約 14 日間
- 技術: Spring Boot + React + Vite + TypeScript
- GitHub Issue: 23 個（全てクローズ）
- テスト: バックエンド約 29 件 + フロントエンド約 28 件

## 📚 学んだこと

### バックエンド

- Spring Boot REST API の設計パターン（Entity → Repository → Service → Controller）
- 各層のテスト手法の使い分け
  - @DataJpaTest: DB アクセスの検証
  - Mockito: Service のビジネスロジック検証（DB なし）
  - @WebMvcTest + MockMvc: HTTP リクエスト/レスポンスの検証
- @RestControllerAdvice による統一エラーハンドリング
- Bean Validation（@NotBlank, @Size）
- DTO パターン（Entity を直接返さない理由）
- @Transactional の使い分け（readOnly）
- springdoc のバージョン互換性問題

### フロントエンド

- React + Vite + TypeScript のプロジェクト構成
- カスタム Hook によるロジック分離（useTodos）
- CSS Modules でのスコープ付きスタイリング
- Vitest（Jest 互換のテストランナー）
- React Testing Library（ユーザー視点のテスト）
- MSW（ネットワークレベルのモック）
- import.meta.env による Vite の環境変数

### 開発プロセス

- GitHub Issue 駆動開発のフロー
- ラベル・マイルストーン管理
- コミットメッセージと Issue のリンク
- GitHub Actions CI の設定

## 💡 苦労した点・解決方法

- springdoc 2.3.0 と Spring Boot 3.5.x の互換性問題 → 2.8.x に更新で解決

## 📈 次のプロジェクトに活かすこと

- GitHubのCI設定をはじめに書いて、自動テストが実行されるようにする
- オンメモリのDBではなく、永続化されるDBに保存されるアプリを作る

## 🔗 リポジトリ

- https://github.com/TYMtwilight/todo-app
