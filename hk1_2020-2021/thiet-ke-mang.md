 ## Thiết kế mạng:
> Thiết kế mạng là một quá trình xây dựng một hệ thống với các công nghệ sẵn có đẻ có thể thỏa mãn được nhu cầu của doanh nghiệp, góp phần vào thành công của doanh nghiệp
### Phân tích yêu cầu:
Việc phân tích yêu cầu của doanh nghiệp đóng vai trò quan trọng trong quá trình thiết kế mạng cho 1 hệ thống, tổ chức. Thông qua quá trình đó, người thiết kế có thể tìm hiểu được cơ cấu và tổ chức của hệ thống mạng đối với doanh nghiệp, từ đó chọn các thiết bị và công nghệ phù hợp cho hệ thống.
- Phân tích mục tiêu và ràng buộc của doanh nghiệp
- Phân tích mục tiêu và vấn đề kỹ thuật.
- Tìm hiểu hệ thống mạng hiện tại.
- Tìm hiểu lưu lượng mạng.

### Thiết kế mạng Logic
- Thiết kế mô hình mạng.
- Thiết kế mô hình địa chỉ và tên.
- Chọn giao thức routing và switching.
- Phát triển giải pháp bảo mật và quản lý.

### Thiết kế mạng vật lý
- Lựa chọn thiết bị và công nghệ phù hợp đối với từng loại mạng (Campus hay Enterprise)

### Kiểm tra, cải tiến và văn bản hóa
- Kiểm tra mô hình mạng có hoạt động ổn định hay chưa,...
- Chỉnh sửa và cập nhật nếu thấy cần chỉnh sửa.
- Văn bản hóa, báo cáo, tài liệu hướng dẫn cho mô hình mạng hiện tại.

## Mức độ ưu tiên:
1. Tính di động - Mobility
2. Bảo mật - Security
3. Khả năng phục hồi - Resiliency
4. Tính liên tục sau sự cố
5. Mục tiêu và chi phí
6. Đảm bảo độ trễ thấp với các ứng dụng real-time.

---------------------------

# CHAPTER 2

## Mục tiêu kỹ thuật
- Tính mở rộng - Scalability
- Tính sẵn sàng - Availability
- Hiệu năng - Performance
- Bảo mật - Security
- Tính quản lý - Manageability
- Tính sử dụng - Usability
- Khả năng đáp ứng - Adaptability
- Khả năng chi trả - Affordability

### Tính sẵn sàng
| (%)     | Per Hour | Per Day | Per Week | Per Year |
|:----:   | :----:   | :----:  | :----:   | :----:   |
| 99.999  | 0.0006   | 0.01    | 0.10     | 5        |
| 99.98   | 0.012    | 0.29    | 2        | 105      |
| 99.95   | 0.03     | 0.72    | 5        | 263      |
| 99.90   | 0.06     | 1.44    | 10       | 526      |
| 99.70   | 0.18     | 4.32    | 30       | 1577     |

```
  Availability = MTBF/(MTBF + MTTR)
  
  MTBF: Mean Time Between Failure 
  MTTR: Mean Time To Repair
```
### Hiệu năng
Các yếu tố ảnh hưởng:
- Băng thông
- Throughput
- Bandwidth utilization
- Offered load
- Accuracy (Sự chính xác)
- Efficiency
- Độ trễ của mạng
- Thời gian phản hồi

**Độ trễ:**
```
  d(nodal) = d(proc) + d(queue) + d(trans) + d(prop)

  d(proc): Xử lý tại nút - Rất nhỏ
  d(queue): Độ trễ xếp hàng
  d(trans): Trễ do truyền = L/R (Chiều dài bits / Băng thông bps )
  d(prop): Trễ do lan truyền d/s (Đồ dài vật lý / tốc độ lan truyền ~ 2.10^8m.s)
```

# CHIA SUBNET

```
  m = 32 - n - SUBNET_MASK_HIEN_TAI

  B1: Số subnet: 2^n
  B2: Số host: 2^m - 2
  B3: Bước nhảy 2^m
  B4: Subnetmask mới 256 - Bước nhảy
  B5: Các Subnet ID gồm
    + Subnet ID đầu tiên = 0
    + Subnet ID kế tiếp = Subnet hiện tại + Bước nhảy
  B6: Trong Subnet ID.
    + Host đầu: Subnet ID + 1
    + Host cuối: Subnet ID + Bước nhảy – 2
    + Địa chỉ Broadcast: Host cuối + 1
```