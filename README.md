# FIT4110 Lab 02 + Lab 03 - IoT Ingestion

Bộ này kết hợp:

- Lab 02: `contracts/openapi.yml` và `contracts/iot-ingestion.openapi.yaml`
- Lab 03: Prism Mock Server, Postman Collection, Newman, CI, checklist, matrix, handshake

## Cài đặt

```bash
npm install
```

## Lint OpenAPI contract

```bash
npm run lint
```

Kết quả lưu tại:

```txt
reports/contract-lint-report.txt
```

## Chạy mock IoT

```bash
npm run mock:iot
```

Mock IoT chạy ở:

```txt
http://localhost:4010
```

## Chạy mock AI Vision cho consumer-side smoke test

Mở terminal thứ hai:

```bash
npm run mock:vision
```

Mock AI Vision chạy ở:

```txt
http://localhost:4011
```

## Chạy Postman Collection bằng Newman trên mock

```bash
npm run test:mock
```

Report sinh trong thư mục `reports/`.

## Chạy trên local service thật

Nếu service thật chạy ở `http://localhost:8000`:

```bash
npm run test:local
```

Nếu chưa code service thật xong, ghi chú trong báo cáo: local environment chưa hoàn thiện, mới kiểm thử được mock theo contract.

## Lưu ý

Collection không hardcode `baseUrl` hoặc `authToken`. Các giá trị này nằm trong Postman Environment.
