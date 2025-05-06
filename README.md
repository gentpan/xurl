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
