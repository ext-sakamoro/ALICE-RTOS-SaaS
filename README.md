# ALICE-RTOS SaaS

Math-first real-time OS scheduler API

## License

AGPL-3.0

## Architecture

```
Frontend :3000  -->  API Gateway :8080  -->  Core Engine :8081
```

| Layer | Port | Technology |
|-------|------|-----------|
| Frontend | 3000 | Next.js 14, Tailwind CSS |
| API Gateway | 8080 | Rust, Axum |
| Core Engine | 8081 | Rust, Axum, ALICE-RTOS |

## Endpoints

| Method | Path | Description |
|--------|------|-------------|
| `POST /api/v1/schedule` | 方程式スケジューリング |
| `GET  /api/v1/tasks` | タスク一覧 |
| `GET  /api/v1/metrics` | リアルタイムメトリクス |
| `GET`  | `/health` | ヘルスチェック |

## Quick Start

```bash
cd services/core-engine
cargo run --release
curl http://localhost:8081/health
```

## Author

Moroya Sakamoto
