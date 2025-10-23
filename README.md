
### Hướng dẫn sử dụng báo cáo và file cấu hình

### Tổng quan
Báo cáo này trình bày thiết kế và cấu hình một hệ thống mạng doanh nghiệp tích hợp cả IPv4 và IPv6. File cấu hình Packet Tracer (pkt) đi kèm chứa mô hình mạng tương ứng, bao gồm các router, switch, và thiết bị khác, được thiết lập dựa trên các phần đã mô tả trong báo cáo.

### Nội dung file cấu hình
- **Tên file**: [configuration.pkt].
- **Phiên bản Packet Tracer**: Được tạo và kiểm tra trên Packet Tracer phiên bản 8.2.2.
- **Cấu hình chính**:
  - Kết nối PPP giữa các router.
  - Thiết lập GRE tunnel.
  - Định tuyến với OSPF (chi nhánh) và EIGRP (HQ).
  - Chuyển mạch với VLAN, VTP, Rapid PVST+, và EtherChannel.
  - NAT, DHCP, và ACL cho IPv4.
  - Cấu hình địa chỉ, định tuyến EIGRPv6, và DHCPv6 cho IPv6.
- **Thiết bị**: Bao gồm các router (R1-R8, ACCESS) model cisco ISR4321, switch (S0-S4) model cisco IOS2960, và các host trong các VLAN.

### Hướng dẫn sử dụng
1. **Mở file**: Sử dụng Packet Tracer để mở file pkt. Đảm bảo phiên bản phần mềm tương thích.
2. **Kiểm tra cấu hình**:
   - Vào chế độ CLI trên từng thiết bị (router, switch) để xem các lệnh cấu hình bằng cách nhập `show running-config`.
   - Kiểm tra kết nối bằng lệnh `ping` giữa các thiết bị (ví dụ: từ R4 đến R5).
   - Xem bảng định tuyến với `show ip route` (IPv4) hoặc `show ipv6 route` (IPv6).
3. **Xem lệnh cấu hình chi tiết**:
   - Mở thư mục "Commands" đi kèm để tham khảo các file lệnh cấu hình chi tiết, bao gồm:
     - IPv4_ACL.txt: Cấu hình ACL cho IPv4.
     - IPv4_Configuration.txt: Cấu hình tổng quát IPv4.
     - IPv4_NAT_DHCP.txt: Cấu hình NAT và DHCP cho IPv4.
     - IPv4_PPP_GRE.txt: Cấu hình PPP và GRE.
     - IPv4_Routing.txt: Cấu hình định tuyến IPv4.
     - IPv6_Configuration.txt: Cấu hình tổng quát IPv6.
     - IPv6_DHCP.txt: Cấu hình DHCPv6.
     - IPv6_Routing.txt: Cấu hình định tuyến IPv6.
   - Các file này chứa các lệnh được áp dụng trên từng thiết bị, được lưu lại vào ngày 11/05/2025.
4. **Thử nghiệm**:
   - Kiểm tra NAT bằng cách truy cập Internet từ host trong VLAN.
   - Xác nhận DHCP/DHCPv6 bằng cách kiểm tra địa chỉ IP được cấp cho host.
   - Thử truy cập bị chặn bởi ACL để kiểm tra hiệu quả.

### Lưu ý
- Đảm bảo tất cả các thiết bị trong mô hình được bật nguồn (Power On) trước khi kiểm tra.
- Nếu gặp lỗi, kiểm tra lại kết nối cáp và trạng thái interface (lệnh `show ip interface brief`).
- Các file trong thư mục "Commands" chỉ mang tính tham khảo, không thay thế cấu hình trực tiếp trên Packet Tracer. Vui lòng đối chiếu với mô hình pkt để đảm bảo tính chính xác.
- Báo cáo đi kèm cung cấp chi tiết về từng bước cấu hình và kết quả đạt được, vui lòng tham khảo để đối chiếu.

### Bản quyền
Bản báo cáo và file cấu hình này thuộc bản quyền của Võ Mạnh Cường - Copyright © Chooky. Mọi sao chép, phân phối hoặc sử dụng trái phép đều không được phép mà không có sự đồng ý bằng văn bản từ Võ Mạnh Cường.

### Thông tin liên hệ
- Tác giả: [Võ Mạnh Cường] AKA [Chooky].
- Mã số sinh viên: [52200319]
- Ngày hoàn thành: 13 tháng 5 năm 2025.
- Phản hồi: [vmcchooky@gmail.com],
            [facebook.com/chooky.vmc].
