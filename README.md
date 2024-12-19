# <center>FINAL PROJECT<center>

### Đồ án thực hành cuối kỳ 
#### Môn: Nhập môn Khoa học Dữ liệu
#### Nhóm: 13 - Lớp 22_21
| HỌ TÊN                | MSSV      |
|:------------------    |:--------: |
| Trần Mạnh Hùng  | 22120117|
| Nguyễn Thị Anh Thi| 22120339  |
| Dương Ngọc Kiều Trinh  | 22120389  |
| Nguyễn Đoàn Minh Uyên  | 22120421  |
| Nguyễn Phạm Tú Uyên  | 22120422  |

# Chủ đề: Phân tích những yếu tố ảnh hưởng tới thị hiếu khán giả và dự đoán xu hướng phim trong tương lai

## Nguồn
#### Nguồn dữ liệu: 
**Các trang web phim:** JustWatch, OMDb API.
#### Nguồn tham khảo:
1. [JustWatch API](https://www.justwatch.com/us/api)
2. [OMDb API Documentation](https://www.omdbapi.com/)
3. Nguồn dữ liệu mở: Kaggle
4. Các trang web phim nổi tiếng: Netflix, VTVGiaitri, FPTPlay

## Nội dung
## Contents
1. **Giới thiệu**
- **Mục tiêu**:
  - Phân tích các yếu tố ảnh hưởng đến thị hiếu khán giả đối với phim điện ảnh
  - Dự đoán xu hướng phim tương lai
- **Phương pháp**:
  - Sử dạng các công cụ phân tích dữ liệu của Python: Pandas, Numpy, Matplotlib, Seaborn và Scikit-learn
  - Áp dụng các thuật toán học máy để dự đoán
2. **Khám phá dữ liệu**
- **Mô tả dữ liệu**:
  - Tổng hợp dữ liệu từ các nguồn(JustWatch, OMDb API)
  - Đặc trưng: Tên, thời gian phát hành, độ tuổi, thời lượng, thể loại, ngôn ngữ, số lượng/tên giải thưởng, điểm từ Metacritic, điểm trên IMDb, số lượt bình chọn, doanh thu nội địa
3. **Đặt câu hỏi ý nghĩa - Tiền xử lí - Phân tích để trả lời câu hỏi - Mô hình dự đoán**
- **Đặt câu hỏi ý nghĩa**:
  1. Với từng thể loại khác nhau thì đánh giá của khán giả khác nhau như thế nào?
     - Giúp xác định thể loại được khán giả yêu thích nhất và thể loại ít được quan tâm, để hiểu rõ xu hướng xem phim.
     - Dựa vào cột IMDb Rating, IMDb Votes, và các thể loại phim.
  2. Các phim thuộc thể loại nào có nhiều khả năng được đề cử hoặc giành giải thưởng nhất?
     - Giúp nhà làm phim định hướng chọn thể loại để tăng khả năng được đánh giá cao.
     - Dựa vào cột Win, Nomination, và các thể loại phim.
  3. Nhóm tuổi (Age rating) ảnh hưởng thế nào đến sự phổ biến của các thể loại phim qua số lượt bình chọn IMDb?
     - Hiểu rõ mức độ quan tâm và xu hướng thị trường.
     - Dựa vào cột Age rating, IMDb Votes, và các thể loại phim
  4. Thời lượng phim (Runtime) ảnh hưởng như thế nào đến số lượng IMDb Votes và IMDb Rating?
     - Xác định thời lượng lý tưởng giúp tăng đánh giá và thu hút khán giả.
     - Dựa vào cột Runtime, IMDb Votes, và IMDb Rating.
  5. Thể loại nào có xu hướng phát triển mạnh nhất qua các quý của năm dựa trên số lượng phim phát hành?
     - Phân tích xu hướng tăng trưởng để định hướng đầu tư vào các thể loại tiềm năng.
     - Dựa vào cột Release time và các thể loại phim.
- **Tiền xử lý**:
  - Tổng hợp dữ liệu 
  - Kiểm tra số lượng cột, dòng và kiểu dữ liệu của từng đặc trưng 
  - Ý nghĩa của từng cột dữ liệu 
  - Phân bố dữ liệu của những cột quan trọng 
  - Xử lí giá trị trùng lặp và giá trị thiếu
- **Phân tích để trả lời câu hỏi**:
- Câu hỏi 1:
    - Phương pháp: Tính điểm trung bình (Bayesian Average) cho IMDb Rating từng thể loại.
    - Trực quan: Biểu đồ bar so sánh IMDb Rating trung bình theo thể loại.
    - Kết luận: Drama phổ biến nhưng đánh giá trung bình; History, Biography được đánh giá cao.

Câu hỏi 2:

Phương pháp: Tính tổng số đề cử và giải thưởng cho từng thể loại.

Trực quan: Bar chart số đề cử và giải thưởng.

Kết luận: Drama dẫn đầu, các thể loại như Adventure, Comedy có tiềm năng.

Câu hỏi 3:

Phương pháp: Tính tỷ trọng IMDb Votes cho từng nhóm tuổi và thể loại.

Trực quan: Bar chart số IMDb Votes trung bình và heatmap tỷ trọng IMDb Votes.

Kết luận: PG-13 và R là nhóm đóng góp chính; Animation, Family hút khán giả nhỏ.

Câu hỏi 4:

Phương pháp: Phân tích IMDb Votes và IMDb Rating theo nhóm thời lượng.

Trực quan: Bar chart số lượng IMDb Votes và IMDb Rating theo Runtime.

Kết luận: Phim >120 phút chất lượng cao; phim 80-120 phút phụ hợp thương mại.

Câu hỏi 5:

Phương pháp: Phân tích số phim phát hành qua các quý theo thể loại.

Trực quan: Line chart xu hướng số lượng phim phát hành theo quý.

Kết luận: Drama, Documentary, Comedy tăng ổn định; Short và Western có xu hướng giảm.
  
4. References
- [1] Cox, R., Kaashoek, M. F., & Morris, R. (2024). xv6: A simple, Unix-like teaching operating system (Revision 4). Massachusetts Institute of Technology. Retrieved from https://pdos.csail.mit.edu/6.1810/2024/xv6/book-riscv-rev4.pdf 
- [2] Pike, R. (n.d.). Notes on threads. Retrieved from https://swtch.com/~rsc/thread/ 
- [3] https://verificationglasses.wordpress.com/2021/01/17/a-star-sokoban-planning/ 
