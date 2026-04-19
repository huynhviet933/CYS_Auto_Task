# CYS_Auto_Task

        HƯỚNG DẪN SỬ DỤNG TOOL CLAIMYSHARE PRO (AUTO TASK & SCAN SOL)

1. YÊU CẦU HỆ THỐNG
- Máy tính đã cài đặt Node.js (Tải tại: https://nodejs.org/)
- Có kết nối Internet ổn định và Proxy sạch (nếu chạy nhiều tài khoản).

2. CÀI ĐẶT THƯ VIỆN (Mở CMD tại thư mục tool và chạy lệnh sau)
--------------------------------------------------------------------------
npm install axios https-proxy-agent colors uuid @solana/web3.js bs58 node-machine-id fs-extra
--------------------------------------------------------------------------

3. CHUẨN BỊ CÁC FILE DỮ LIỆU (Tạo cùng thư mục với file tool)
- token.txt        : Dán danh sách Token Bearer (mỗi dòng 1 cái).
- proxy.txt        : Dán danh sách Proxy (ip:port hoặc user:pass@ip:port).
- User_agents.txt  : Dán danh sách User Agent (mỗi dòng 1 cái).
- config.json      : Copy nội dung cấu hình bên dưới và lưu lại.

MẪU FILE config.json:
{
  "threads": 3,
  "threadGap": 10,
  "actionDelay": [3, 7],
  "boxDelay": [10, 15],
  "accountDelay": [30, 60]
}

* Giải thích: 
  - threads: Số luồng (số tài khoản chạy cùng lúc).
  - actionDelay: Delay làm nhiệm vụ (giây).
  - boxDelay: Delay mở hộp (giây).
  - accountDelay: Delay chuyển ví (giây).

4. CÁC TÍNH NĂNG CHÍNH CỦA TOOL
- Login & Check Balance: Tự động đăng nhập và kiểm tra số dư CYS, SOL.
- Tự động Quét (Scan) ví SOL: 
  + Nếu tài khoản chưa gắn ví, tool tự tạo ví SOL mới.
  + Thực hiện Scan và Claim để nhận ngay 5000 CYS.
  + Thông tin ví được gắn cố định vào Token qua file profiles.json.
- Auto Task: Làm toàn bộ nhiệm vụ chưa hoàn thành.
- Auto Open Box: Tự động mở toàn bộ Mystery Box có trong tài khoản (Delay 10-15s).
- Lưu kết quả: Ghi toàn bộ Private Key và số dư SOL vào file SOL.txt.

5. CÁCH CHẠY TOOL
- Mở Terminal/CMD gõ lệnh: node tên_file.js (Ví dụ: node p1.js)
- Nhập License Key khi được yêu cầu (Key sẽ tự lưu vào file license.txt).

6. LƯU Ý QUAN TRỌNG
- File SOL.txt sẽ lưu theo định dạng: Privatekey | Địa chỉ ví | Số dư SOL.
- KHÔNG ĐƯỢC XÓA file profiles.json vì đây là nơi lưu trữ ví SOL đã gắn cho Token.
- Tool có cơ chế đọc file động: Bạn có thể thêm Proxy hoặc Token vào file txt ngay cả khi tool đang chạy.

==========================================================================

Tham Gia NHóm tele : https://t.me/HVchannelss

Tham Gia Discor ( Vip ) : https://discord.gg/gKxvTNu5

Tham gia NHóm VIp Với Chi Phí 1 Tháng 4u - 15u 6thang Lợi ích tham gia nhóm ViP Sẽ được cấp keey sử dụng các tool vip trong discor hỗ trợ Và tham khao Code các tool dự án mà các bạn đề xuất

Gửi Phí tháng vào đây và chụp hình gửi trực tiếp cho tôi tại discor để xác nhận Role VIp ☕ https://huynhviet933.github.io/donate_viet_mmo/ Có thể tặng tôi ít cafe tại đây

Donenat : https://huynhviet933.github.io/donate_viet_mmo/
