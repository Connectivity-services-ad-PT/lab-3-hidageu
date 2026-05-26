# Consumer-side Smoke Testing

Consumer-side smoke test trong collection gọi mock của service phụ thuộc, không chỉ gọi lại API của chính IoT Service.

Request dùng trong collection:

```txt
POST {{aiVisionMockUrl}}/detect
```

Biến `aiVisionMockUrl` nằm trong Postman Environment.
