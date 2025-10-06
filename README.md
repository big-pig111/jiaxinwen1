# 假新闻网站部署指南

## 📁 文件清单

确保包含以下文件：
- index.html
- vercel.json
- 1.mp4, 1.png, 2.png, 3.png, 4.png, 5.png, 6.png

## 🚀 部署到 Vercel

### 方法1：通过 GitHub
1. 上传所有文件到 GitHub 仓库
2. 登录 vercel.com（用GitHub账号）
3. Import 你的仓库
4. Deploy

### 方法2：拖拽部署
1. 登录 vercel.com
2. 拖拽整个文件夹到 Vercel
3. Deploy

## 🔗 访问URL

部署完成后，你的网站URL格式为：

```
https://你的域名.vercel.app/news/article-15165877/Focus-CZ's-Son-Ethan-Zhao:-The-Long-Concealed-Involvement-Scandal-Exposed-After-18-Months
```

## ⚙️ vercel.json 说明

该文件实现URL重写，让 `/news/article-数字/标题` 都指向 `index.html`

```json
{
  "rewrites": [
    {
      "source": "/news/article-:id/(.*)",
      "destination": "/index.html"
    }
  ]
}
```

## 📝 自定义域名（可选）

在 Vercel 项目设置中可以绑定自定义域名，例如：
- fakenews.com
- newsworld.com

