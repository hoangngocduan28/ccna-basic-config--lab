# Network Lab: Enterprise Core/Distribution & Access

Dự án này chứa các file cấu hình và sơ đồ cho bài lab mạng mô phỏng kiến trúc doanh nghiệp thu nhỏ với các lớp Core/Distribution và Access.

## Tổng quan hệ thống
Hệ thống mạng bao gồm:
- **Router biên (R6)**: Cửa ngõ kết nối ra "Internet" (Loopback 8.8.8.8).
- **Multilayer Switch (R1, R2)**: Đóng vai trò Core/Distribution, xử lý định tuyến Inter-VLAN và dự phòng.
- **Switch Access (R3)**: Switch truy cập cho các thiết bị đầu cuối.
- **End Devices (VPC4, VPC5)**: Máy tính người dùng thuộc các VLAN 10 và 20.

*(Xem chi tiết cấu trúc mạng trong file `Topo.png`)*

## Thành phần file trong Repository

- `Topo.png`: Sơ đồ mạng tổng quan (Topology).
- `R1.txt`, `R2.txt`: File cấu hình CLI cho Core/Distribution Switch (SVI, HSRP, LACP, STP, Routing).
- `R3.txt`: File cấu hình CLI cho Access Switch (VLAN, Access port, Trunking).
- `R6.txt`: File cấu hình CLI cho Router (IP Addressing, Routing).
- `VPC4.png`, `VPC5.png`: Ảnh chụp cấu hình IP và kết quả test kết nối (ping) từ các VPC.

## Các công nghệ & Giao thức sử dụng
- **Chuyển mạch Layer 2**: VLAN (10, 20), 802.1Q Trunking.
- **Dự phòng & Gộp liên kết**: EtherChannel (LACP), Spanning Tree Protocol (Rapid PVST+).
- **Định tuyến Layer 3**: SVI (Switch Virtual Interface), Static Routing (Default Route tới Internet).
- **Dự phòng Gateway (FHRP)**: HSRP (Hot Standby Router Protocol).