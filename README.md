📖 仓库概述

这是一个基于 Hugo Blox Builder 的学术简历网站项目，专门用于展示研究人员、学者或博士生的个人简历、研究成果和学术资料。

🏗️ 核心技术栈

•  Hugo (v0.150.1) - 静态网站生成器
•  Hugo Blox Builder - 学术网站专用框架
•  Tailwind CSS v4 - 现代CSS框架
•  pnpm - Node.js包管理器
•  GitHub Pages/Netlify - 自动部署

📁 目录结构说明

🔧 配置文件
📝 内容目录 (content/)
🎨 主题和布局
🚀 常用开发命令

本地开发
bash
Hugo原生命令
bash
🔄 自动化工作流

📚 论文自动导入
•  在仓库根目录放置 publications.bib 文件
•  GitHub Actions自动将BibTeX转换为Markdown页面
•  使用Python的academic包处理转换

🚢 自动部署
•  GitHub Pages: 推送到main分支自动部署
•  Netlify: 支持预览部署和分支部署
•  包含自动搜索索引生成

💡 核心特色功能

区块化页面系统
首页使用声明式区块系统，每个部分都是独立的区块：
•  resume-biography-3 - 个人简介区块
•  collection - 内容集合展示
•  markdown - 自定义内容区块

丰富的内容类型
•  个人资料: 教育背景、工作经历、技能、获奖情况
•  学术论文: 支持DOI链接、PDF下载、代码仓库链接
•  研究项目: 项目展示和详细描述
•  学术活动: 会议演讲、讲座等

🎯 使用场景

这个模板特别适合：
•  📖 博士生/研究生制作学术简历
•  🎓 教授/研究员展示研究成果
•  💼 技术人员求职展示
•  📊 学术机构成员介绍页面

🛠️ 快速上手步骤

1. 克隆仓库后：运行 pnpm install
2. 修改个人信息：编辑 content/authors/admin/_index.md
3. 添加研究成果：在 content/publications/ 添加论文
4. 自定义首页：修改 content/_index.md 的区块配置
5. 本地预览：运行 pnpm run dev
6. 部署：推送到GitHub，自动部署到GitHub Pages

这个仓库结构非常适合学术人员快速搭建专业的个人网站，展示研究成果和学术资历。
