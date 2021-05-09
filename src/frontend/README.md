# mock up app Documentation

## デフォルトルート
汎用的な動画像処理に対してのルートを提供しています。

### mp4エンコード
入力する動画のパスと、出力するディレクトリのパスを`string`型で渡してください。

```typescript
await mockupApi.encode(input_path, output_dir)
```