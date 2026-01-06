# KoiButler V1

闲鱼自动化管理系统 - 编译版

## 功能特性

- 多账号管理（Cookie 登录）
- 自动回复（精确/包含/正则/AI 智能回复）
- 自动发货（虚拟发货/免拼发货）
- 自动退款（未发货订单自动同意）
- 订单管理
- 商品管理
- 工作流引擎
- 多用户支持（数据隔离）

## 运行

```bash
# Linux/macOS
chmod +x koi-butler
./koi-butler

# 默认端口 13456
# 访问 http://localhost:13456
```

## 环境变量

| 变量 | 默认值 | 说明 |
|------|--------|------|
| `SERVER_PORT` | 13456 | HTTP 服务端口 |
| `DB_PATH` | data/koi-butler.db | SQLite 数据库路径 |
| `JWT_SECRET` | (内置) | JWT 签名密钥 |
| `LOG_LEVEL` | INFO | 日志级别 |

## 目录结构

```
KoiButlerV1/
├── koi-butler          # 可执行文件 (Linux ARM64)
├── frontend/
│   └── dist/           # 前端静态文件 (必须保持此路径)
└── README.md
```

## 注意事项

- 当前编译版本为 **Linux ARM64** 架构
- **前端文件必须放在 `frontend/dist/` 目录下**
- 首次运行会自动创建 `data/` 和 `logs/` 目录
- 默认管理员账号需要首次访问时注册

## 技术栈

- 后端: Go + Chi Router + SQLite
- 前端: Vue 3 + TypeScript + Element Plus
- 通信: WebSocket + REST API
