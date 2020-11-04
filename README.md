# foo-controller-kubebuilder

- Kubebuilder PROJECT の初期化
- Kubebuilder で、API Object と Controller のテンプレートを作成
- types.go を編集して、API Object を定義
- controller.go を編集して、Reconcile を実装
  - もろもろ import
  - RBAC Marker を必要に応じて追加
  - Reconcile 関数の修正
    - Foo Object を in-memory-cache から取得する
    - 古い Deployment が存在していたら削除する
    - Foo が管理する Deployment を作成または更新する
    - Foo ステータスを更新する
