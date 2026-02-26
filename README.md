# 数字易经 - Digital I Ching Divination Tool

一款基于传统铜钱占卜法的在线易经占卜工具，包含完整六十四卦数据。

## 项目结构

```
digital-yijing/
├── index.html          # 主页面（HTML 结构）
├── css/
│   └── style.css       # 样式文件（所有 CSS）
├── js/
│   └── app.js          # 逻辑脚本（六十四卦数据 + 交互逻辑）
└── README.md           # 项目说明
```

## 功能特点

- 🎴 铜钱翻转 3D 动画
- 📊 六爻卦象逐步生成
- 📖 完整六十四卦卦辞
- 📱 响应式设计，适配移动端

## 部署方式

### 1. 静态托管（推荐）

纯前端项目，无需后端。可直接部署到：

- **GitHub Pages** — 推送到仓库，开启 Pages 即可
- **Vercel** — `vercel deploy`
- **Netlify** — 拖拽文件夹上传或连接 Git 仓库
- **Cloudflare Pages** — 连接 Git 仓库自动部署

### 2. Nginx 部署

```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /var/www/digital-yijing;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

### 3. 本地预览

```bash
# 使用 Python
python3 -m http.server 8080

# 或使用 Node.js
npx serve .
```

然后访问 `http://localhost:8080`

## 外部依赖

- [Google Fonts](https://fonts.google.com/) — Noto Serif SC & ZCOOL XiaoWei 字体（通过 CDN 加载）

## 许可

MIT License
