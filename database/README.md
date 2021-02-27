# database

storeを使ってよろしくやってくれるやつ

## memo

- storeを抽象化して扱うようにしてみた
- 考えてみたら「このデータはこのデータストアに出し入れする」ということがある一定決まっていて、特に長いスパンで見て変更予定もなさそうと言うのであれば、特定のstoreの実装に依存させても良いのでは
- 複数のデータソースにデータを分散させたいという場合にはstoreを抽象化しておくと利点がありそう
  - 抽象化されたstoreはそういった特定の用途を前提とするのであれば、「なんでもできる」というよりはその「特定の用途を満たせる」ようなinterfaceになっていると良さそう
  - 「なんでもできる」ようなinterfaceはメンテナンスと実装が大変そうなので