**Phần 1. Báo cáo phân tích I/O**

Khi lập trình dự án JavaScript, luồng dữ liệu từ lúc nhấn Ctrl + S đến khi xuất hiện tích xanh diễn ra như sau:

1.  Nhấn Ctrl + S: Code được lưu vào ổ SSD Local, giúp truy cập và chỉnh sửa nhanh.
    
2.  Phần mềm Cloud Sync phát hiện file thay đổi và đưa file vào hàng đợi đồng bộ.
    
3.  Dữ liệu được tải lên Cloud thông qua Internet.
    
4.  Cloud lưu phiên bản mới của file.
    
5.  Khi đồng bộ thành công, biểu tượng tích xanh xuất hiện, báo hiệu file đã được đồng bộ.
    

**Phần 2. Thiết kế Hybrid Workflow**

1.  Tổ chức thư mục dự án trên ổ SSD Local để lập trình nhanh.
    
2.  Đồng bộ thư mục dự án lên Google Drive hoặc OneDrive để bảo vệ source code.
    
3.  Sử dụng Files On-Demand để xem và truy cập file trên Cloud mà không cần tải toàn bộ xuống máy. Khi cần sử dụng, file sẽ được tải về.
    
4.  Bật Version History để có thể khôi phục phiên bản cũ khi code bị sửa hoặc xóa nhầm.
    
5.  Sử dụng Git và GitHub để quản lý lịch sử thay đổi code và hỗ trợ làm việc nhóm.

**Phần 4. Xử lý bẫy dữ liệu node_modules**

-   Tạo file .gitignore trong thư mục dự án và thêm dòng node_modules/ để Git không đưa thư mục này vào quản lý mã nguồn.
    
-   Cấu hình phần mềm Cloud Sync để loại trừ node_modules nếu phần mềm hỗ trợ.
    
-   Giữ lại package.json và package-lock.json để có thể cài đặt lại các thư viện bằng lệnh npm install khi cần.
    
-   Chỉ đồng bộ source code, tài liệu và tài nguyên cần thiết lên Cloud, tránh đồng bộ hàng vạn file không cần thiết.
    

**Em kết luận như sau:** Hybrid Workflow kết hợp SSD Local, Cloud Sync, Files On-Demand và Git giúp lập trình nhanh, tiết kiệm dung lượng và hạn chế mất dữ liệu. Đặc biệt, loại trừ node_modules giúp quá trình đồng bộ nhẹ hơn mà vẫn bảo vệ được source code chính.
