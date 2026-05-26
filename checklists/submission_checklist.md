# Lab 03 Submission Checklist

- [ ] Contract lint pass hoặc có giải thích rõ warning còn lại.
- [ ] Collection chạy được trên mock environment.
- [ ] Collection chạy được trên local environment, hoặc có ghi chú rõ phần chưa hoàn thiện.
- [x] Collection không hardcode `baseUrl` hoặc `authToken`.
- [x] Có test cho happy path, auth, negative, boundary/reliability.
- [x] Có ít nhất một consumer-side smoke test gọi mock của service phụ thuộc.
- [ ] Newman report được sinh trong thư mục `reports/` sau khi chạy `npm run test:mock`.
- [x] Test-case matrix map được từng test với endpoint, input, expected status và loại test.
- [x] Reliability checklist đã hoàn thiện.
- [x] Consumer-provider handshake đã hoàn thiện.
