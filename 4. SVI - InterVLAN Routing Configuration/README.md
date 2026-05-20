# SVI - InterVLAN Routing Configuration

Lab cấu hình Inter-VLAN Routing sử dụng 1 Core Switch (Layer 3) và 2 Access Switch (Layer 2). Dự án bao gồm sơ đồ phân hoạch IP, kịch bản cấu hình sạch 

### Tính năng triển khai:
* Cấu hình SVI (Switch Virtual Interface) trên Core Switch.
* Cấu hình đường truyền Trunking (802.1Q) mã hóa đồng bộ `duplex full`.
* Phân chia VLAN 100 (Server), 101, 102 về đúng các cổng Access.
* Kiểm tra định tuyến toàn mạch (End-to-End Ping).

## Sơ đồ mạng (Topology)
![Sơ đồ mạng](Topo.png)

## Các file cấu hình thiết bị
* [Cấu hình chi tiết Core      ](Core.txt)
* [Cấu hình chi tiết Access_01 ](Access_01.txt)
* [Cấu hình chi tiết Access_02 ](Access_02.txt)
* [Cấu hình chi tiết Server    ](Server.txt)
* [Cấu hình chi tiết vPC5      ](vPC5.txt)
* [Cấu hình chi tiết vPC6      ](vPC6.txt)
* [Cấu hình chi tiết vPC7      ](vPC7.txt)
* [Cấu hình chi tiết vPC8      ](vPC8.txt)
* [Cấu hình chi tiết vPC9      ](vPC9.txt)