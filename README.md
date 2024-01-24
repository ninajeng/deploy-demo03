# deploy-demo03

使用 git 指令進行部屬

# 步驟

1. vite.config.js 中， base 屬性設定為儲存庫名稱
```sh
base: "/<REPO>/"
```

2. 編譯專案
```sh
npm run build
```

3. 將專案上傳至 gitHub (SSH)
```sh
git init
git add .
git commit -m 'first commit'
git remote add origin git@github.com:<USERNAME>/<REPO>.git
git branch -M main
git push -u origin main
```

4. 新增 gh-pages 分支，並且部屬編譯後的專案
```sh
git add dist -f
git commit -m 'deploy'
git subtree push --prefix dist origin gh-pages
```

# 參考資料

1. How to Deploy Your Vite App to Github Pages
https://www.youtube.com/watch?v=yo2bMGnIKE8

2. 部署 Vite 專案至 GitHub Pages
https://medium.com/@71080635/%E9%83%A8%E7%BD%B2-vite-%E5%B0%88%E6%A1%88%E8%87%B3-github-pages-6fb0391652a7