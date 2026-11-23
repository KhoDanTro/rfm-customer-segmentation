# Đối chiếu báo cáo Đồ án 1 với kết quả chạy lại

Khớp: số dòng sau từng bước làm sạch, 4.338 và 4.275 khách, ngưỡng 99% (M = 19.881 £, F = 30), K=4: WCSS 3782,76, silhouette 0,3329, DB 1,0177; iK-means K=7: WCSS 2516,54, silhouette 0,2778, DB 1,0487; bảng tỷ trọng doanh thu 7 cụm.

Không khớp (cần sửa trong báo cáo):
1. **Mục 4.2.2 và Bảng 4.1:** báo cáo nói trích xuất 15 tiểu cụm, có cụm C7 (18 khách, M = 46.500 £) được "cứu VIP", và các cụm bị loại có kích thước 2–85. Chạy `ikmeans.py` trên `rfm_cleaned.csv` cho 26 tiểu cụm; 7 cụm được giữ có kích thước 150–1043 và M trung bình lớn nhất 3635,2 £; không có cụm 18 khách nào; các cụm bị loại có kích thước 1–123. Bảng 4.1 cần thay bằng nhật ký thật.
2. **Mục 5.1.1:** báo cáo mô tả "Khách Mới" và "Sắp Rời Bỏ" là vừa ghé gần đây (R cao sau đảo trục). Theo số liệu, cụm mang tên "Khách Mới" (xếp theo M) có R trung bình 178,9 ngày, tức mua đã lâu; cụm mua gần đây (R 35,6, F 1,4) mới là nhóm khách mới/mua lẻ. Tên cụm trong code gán theo thứ hạng M nên hai cụm này bị đảo.
3. **Bảng 4.2:** thời gian iK-means 1,9739 giây khác với lần chạy lại (khoảng 0,09 giây); thời gian phụ thuộc máy, nên ghi rõ cấu hình hoặc bỏ.
