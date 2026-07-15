# 開発方法
## 環境構築
### Rubyのインストール
- [https://rubyinstaller.org/downloads/](https://rubyinstaller.org/downloads/) から `Ruby+Devkit 4.0.5-1 (x64)` をダウンロード．
- インストールはそのまますべてNext．
- MSYS2のインストールのためにcmdが立ち上がるので， （MSYS2をインストールしたことがない人は）`1,3` でEnter
- `succeeded` で終わったら，何も入力せずEnterで閉じる．
- 参考：[https://prog-8.com/docs/ruby-env-win](https://prog-8.com/docs/ruby-env-win)

### Jekyllのインストール
```
gem install jekyll bundler
```

### ローカルサーバー起動
```
bundle exec jekyll serve
```
`http://localhost:4000/` にアクセス