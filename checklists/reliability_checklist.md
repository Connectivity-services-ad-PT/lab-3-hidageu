# Reliability Checklist

| Tiêu chí | Trạng thái | Ghi chú |
|---|---|---|
| Có boundary test | Done | `POST boundary high temperature`, `GET max limit boundary` |
| Không test lại request body đã gửi | Done | Test kiểm tra response/status/header/body từ server |
| Có kiểm tra 429 hoặc rate-limit | Done | Contract có response `429`, collection có test documented behavior |
| Có negative test dữ liệu sai | Done | Missing `deviceId`, invalid enum, invalid query |
| Có auth test | Done | Valid token, missing token, wrong token |
| Không dùng mock latency để kết luận service thật | Done | Latency test chỉ chạy khi `env=local` |
| Có dùng environment variable | Done | `baseUrl`, `authToken`, `aiVisionMockUrl` |
