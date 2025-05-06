# xurl - 轻量级短网址服务

一个基于 **PHP + MySQL + Nginx** 打造的短网址生成与管理系统，专注于极简、快速与易用。

[![License](https://img.shields.io/github/license/yourname/xurl)](LICENSE)

## ✨ 功能特性

- 🚀 短链接生成与跳转
- 🔒 支持私密短链接（可选密码保护或访问次数限制）
- 📊 基本访问统计（IP、浏览器、时间等）
- 🧹 支持自定义短链接别名
- 🧑‍💻 提供简单 API 接口（方便程序调用）
- 🌐 支持 Nginx 优化跳转规则

## 📦 技术架构

- **后端**：PHP 7+（支持 PDO/MySQLi）
- **数据库**：MySQL 5.6+ / MariaDB
- **Web服务器**：Nginx（推荐） / Apache（可选）
- **其他**：可使用 Redis 缓存优化（可选）

## 🚀 快速开始

### 1. 克隆项目

```bash
git clone https://github.com/yourname/xurl.git
cd xurl
2. 导入数据库
导入 database.sql 文件到你的 MySQL 数据库。

sql
复制
编辑
CREATE DATABASE xurl;
USE xurl;
SOURCE database.sql;
3. 配置数据库信息
复制并修改配置文件：

bash
复制
编辑
cp config.sample.php config.php
编辑 config.php 填写数据库相关配置。

4. 配置 Nginx
nginx
复制
编辑
server {
    listen 80;
    server_name your-domain.com;

    root /path/to/xurl;
    index index.php;

    location / {
        try_files $uri $uri/ /index.php?$query_string;
    }

    location ~ \.php$ {
        fastcgi_pass unix:/run/php/php7.4-fpm.sock; # 根据你的PHP版本调整
        fastcgi_index index.php;
        include fastcgi_params;
        fastcgi_param SCRIPT_FILENAME $document_root$fastcgi_script_name;
    }
}
5. 访问与使用
部署完成后，访问你的域名，即可使用 xurl 短网址服务！

📖 API 说明（可选）
创建短链接

查询短链接状态

（API 文档请见 API.md 文件或访问项目文档页面）

📌 TODO
短链接批量生成

后台管理界面

登录权限控制

📄 License
MIT License

项目由 yourname 维护。欢迎提交 Issue 和 PR 共建。

yaml
复制
编辑

---

## 🏷 推荐 GitHub Topics 标签（创建时添加）

在 GitHub 创建项目时，记得填一下这些标签（Topics）：

php, url-shortener, nginx, mysql, url, link, shortener, api, self-hosted
