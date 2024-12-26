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
3. **Tiền xử lí - Đặt câu hỏi ý nghĩa - Mô hình dự đoán**   
- **Tiền xử lý**:
  - Tổng hợp dữ liệu 
  - Kiểm tra số lượng cột, dòng và kiểu dữ liệu
  - Xử lí giá trị trùng lặp và giá trị thiếu
 
- **Đặt câu hỏi ý nghĩa**:
  1. Với từng thể loại khác nhau thì đánh giá của khán giả khác nhau như thế nào?
  2. Các phim thuộc thể loại nào có nhiều khả năng được đề cử hoặc giành giải thưởng nhất?
  3. Nhóm tuổi (Age rating) ảnh hưởng thế nào đến sự phổ biến của các thể loại phim qua số lượt bình chọn IMDb?
  4. Thời lượng phim (Runtime) ảnh hưởng như thế nào đến số lượng IMDb Votes và IMDb Rating?
  5. Thể loại nào có xu hướng phát triển mạnh nhất qua các quý của năm dựa trên số lượng phim phát hành?

- **Mô hình dự đoán**:
  1. Dự đoán phim có thành công hay không (Ratings > 7.0).
    - Mục tiêu: Hiểu rõ các yếu tố ảnh hưởng đến sự thành công của bộ phim.
  2. Dự đoán Ratings của phim.
    - Mục tiêu: Dự đoán IMDb Rating dựa trên thời lượng, giới hạn độ tuổi, thể loại, lượt đề cử, thắng giải và bình chọn.
4. **References**
- [1] API reference. (n.d.). Scikit-Learn. Retrieved December 19, 2024, from https://scikit-learn.org/1.5/api/index.html 
- [2] API reference — pandas 2.2.3 documentation. (n.d.). Pydata.org. Retrieved December 19, 2024, from https://pandas.pydata.org/docs/reference/ 
- [3] Matplotlib documentation — Matplotlib 3.9.3 documentation. (n.d.). Matplotlib.org. Retrieved December 19, 2024, from https://matplotlib.org/stable/ 
- [4] API reference — seaborn 0.13.2 documentation. (n.d.). Pydata.org. Retrieved December 19, 2024, from https://seaborn.pydata.org/api.html 
- [5] Using the Bayesian average in custom ranking. (n.d.). Algolia Documentation. Retrieved December 19, 2024, from https://www.algolia.com/doc/guides/managing-results/must-do/custom-ranking/how-to/bayesian-average/

## Cấu trúc dự án
```plaintext
IntroDS/
|- Data/
   |- links.txt
   |- movie_data.csv
   |- movie_data_part1.csv
   |- movie_data_part2.csv
   |- movie_data_part3.csv
   |- pre_data_part1.csv
   |- pre_data_part2.csv
   |- pre_data_part3.csv
|- Source_codes/
   |- AnsweringQuestion.ipynb
   |- DataCollection_part1.ipynb
   |- DataCollection_part2.ipynb
   |- DataPreprocessing.ipynb
   |- LinkCollecting.ipynb
   |- MachineLearning_part1.ipynb
   |- MachineLearning_part2.ipynb
   |- Reflection.ipynb   
|- README.md
```
## Hướng dẫn sử dụng
#### Yêu cầu hệ thống
- Python
- Thư viện cần thiết
  - Pandas
  - Numpy
  - Matplotlib
  - Seaborn
  - Scikit-learn

#### Hướng dẫn cài đặt
```bash
git clone https://github.com/alpaca3000/IntroToDS
cd IntroToDS/Source_codes
jupyter notebook DataPreprocessing.ipynb AnsweringQuestion.ipynb ML_1.ipynb ML2.ipynb
```
