# Hoạt động
1. `Prometheus` (cấu hình external_labels) config chế độ `remote_write` đến url "http://thanos-receive-1:10803/api/v1/receive" của `thanos-receive-1`
2. `Thanos-Receive` nhận dữ liệu từ Prometheus. Data được phân phối đến các `Thanos-Receive` thông qua config hashring. Các `Thanos-Receiver` hỗ trợ việc sao chép series-time trong cùng một `hashring`(flag `--receive.replication-factor`)
3. `Thanos-Receive` đẩy dữ liệu vào MINIO(flag `--objstore.config-file`) bucket Thanos theo block
4. `Thanos-Query` thực hiện query dữ liệu từ `Thanos-Receive`(query real-time) và MINIO thông qua `Thanos-Store`.
5. `Thanos-Compactor` compact & down sample
