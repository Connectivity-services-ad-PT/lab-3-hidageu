# Consumer-Provider Handshake

## Consumer

- Service: IoT Ingestion
- Mục đích: cần gọi AI Vision để kiểm tra dữ liệu/phụ thuộc trong smoke test.

## Provider

- Service: AI Vision
- Mock contract: `contracts/ai-vision.openapi.yaml`
- Mock URL: `http://localhost:4011`

## Endpoint phụ thuộc

| Provider | Endpoint | Method | Expected status | Ghi chú |
|---|---|---|---|---|
| AI Vision | `/detect` | POST | 200 | Consumer-side smoke test gọi qua `{{aiVisionMockUrl}}/detect` |

## Quy ước

- Consumer không hardcode URL provider.
- URL provider nằm trong biến môi trường `aiVisionMockUrl`.
- Khi provider thật chưa hoàn thiện, consumer dùng Prism mock để kiểm thử sớm.
- Khi provider thật hoàn thiện, đổi `aiVisionMockUrl` sang URL service thật.
