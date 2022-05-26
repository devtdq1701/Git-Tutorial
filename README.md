## Tổng quan về git và github

### Git

- `Git` là tên gọi của một `hệ thống quản lý phiên bản phân tán` (`Distributed Verson Control System - DVCS`), một trong những hệ thống quản lý phiên bản phân tán phổ biến nhất hiện nay.

- `DVCS` giúp mỗi PC có thể `lưu trữ` nhiều phiên bản khác nhau của một bộ source code đã được nhân bản (`clone`) từ 1 kho chứa mã nguồn (`repository`), các thay đổi trên mã nguồn sẽ được `commit` rồi `push` lên server nơi đặt kho chứa chính (`remote repository`). Các PC khác (có quyền truy cập) cũng có thể `clone` lại mã nguồn từ kho chứa để lấy phiên bản mới nhất. Khái niệm này gọi là `working tree`.

- `Git` tối ưu hơn các hệ thống quản lý code thống thường vì có khả năng `branch`, hỗ trợ tốt cho teamwork, vì những việc như phân chia task, tổng hợp code trở nên dễ dàng hơn nhiều.

**Tính chất của git:**

- An toàn, nhanh chóng, dễ sử dụng
- Giúp cho việc làm việc nhóm đơn giản = cách `merge` các `branch`
- Git giống như 1 chuẩn quản lý mã nguồn, giống như `SVN`
- Có nhiều trang hỗ trợ git k chỉ riêng github, như bitbucket

### Github

- 1 cty của Mỹ, hiện tại đã đc microsoft mua lại
- Chuyên cung cấp hosting dịch vụ version control sử dụng git cho software development
- Nhờ đó có thể lưu trữ repo qua internet
- Sự kết hợp hoàn hảo giữa git và github mang lại sự thuận tiện: bạn có thể code của mỉnh ở mọi nơi, k sợ bị ghi đè, bị mất dữ liệu, có thể trở về thời điểm bất kỳ mà bạn thay đổi code

## Tại sao cần version control & git ?

- Theo dõi, kiểm soát thay đổi trong code
- Đồng bộ hóa code giữa mọi ng (git fetch)
- Kiểm tra tính năng mới mà không mất đi tính năng cũ (git branch -> git merge)
- Quay trở lại version cũ hơn (git revert)
