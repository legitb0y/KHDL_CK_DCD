# Dự đoán đánh giá trung bình của sách📚

## ⚙Các thư viện cần cài đặt

| Thư viện  | Lệnh cài đặt                  | Mô tả          |
| :-------  | :---------------------------- | :------------- |
| `bs4`     | `pip install bs4`             | Beautiful Soup |
| `sklearn` | `pip install -U scikit-learn` | scikit-learn   |

## ⏱Chạy chương trình

Crawl dữ liệu từ trang web goodread.com

```bash
  crawl.ipynb
```

File lưu trữ các file dữ liệu thô

```bash
  raw_data.csv
```

Làm sạch dữ liệu chuyển biến về đúng dạng dữ liệu

```bash
  clean.ipynb
```

File lưu trữ dữ liệu được làm sạch

```bash
  data_10000.csv
```

Thống kê mô tả dữ liệu

```bash
  ThongKeMota.ipynb
```

Xử lí dữ liệu và Xây dựng mô hình dự đoán rating book

```bash
  main_10000.ipynb
```

## 👯‍♂️Thành viên
- [Lê Văn Đạt](https://github.com/xenicedtea)
- [Trần Thị Diễm](https://github.com/diemtran2806)
- [Nguyễn Thị Cầm](https://github.com/camnguyen236)

## 👨‍💻·Dữ liệu
 Bộ dữ liệu các thông tin của sách được thu thập từ trang:
 - [goodreads](https://www.goodreads.com/)

## 🔨 Feature engineering
 - Làm sạch dữ liệu, thêm các đặc trưng mới
 - Chuyển dữ liệu dạng chuỗi thành dữ liệu dạng số sử dụng **LabelEncoder** của *sklearn*
 - Thay thế dữ liệu trống bằng giá trị **endOfDist**
 - Xử lý ngoại lệ sử dụng **IQR** để tìm biên trên và biên dưới của dữ liệu
 - Chuẩn hóa dữ liệu sử dụng **PowerTransformer** của *sklearn*

## 💡 Mô hình dự đoán
 - Sử dụng **SupportVectorRegression** của *sklearn*
 - Cải tiến dùng **RandomForestRegressor** của *sklearn*

## 🌌 Các metrics đánh giá
 - **MAE**
 - **RMSE**
 - **R2**

## 🏁 Kết quả dự đoán

| Mô hình          | MAE     | RMSE      | R2       |
| :--------------- | :-----  | :-------- | :--------|
| RFR              | 0.171   | 0.219     | 0.4134   |
| SVR              | 0.1775  | 0.258     | 0.1859   |

