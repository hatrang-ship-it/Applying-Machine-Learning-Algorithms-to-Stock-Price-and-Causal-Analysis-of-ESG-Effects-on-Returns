Chào bạn, dựa trên nội dung báo cáo bạn cung cấp, dưới đây là gợi ý nội dung file `README.md` chuyên nghiệp, đầy đủ để bạn đăng tải lên GitHub.

---

# Applying Machine Learning for Stock Price Forecasting and ESG Causal Analysis

Đây là kho lưu trữ mã nguồn cho dự án nghiên cứu về ứng dụng các thuật toán Machine Learning để dự báo giá cổ phiếu hàng ngày và sử dụng kỹ thuật Double Machine Learning (DML) để phân tích tác động nhân quả của các yếu tố ESG (Môi trường, Xã hội, Quản trị) đến lợi nhuận doanh nghiệp.

## 📝 Tóm tắt dự án

Nghiên cứu này tập trung vào hai mục tiêu chính:

1. **Dự báo giá cổ phiếu:** So sánh hiệu suất của các mô hình Machine Learning (Linear Regression, Ridge, Random Forest, Gradient Boosting, XGBoost) trong việc dự báo giá đóng cửa đã điều chỉnh.
2. **Phân tích nhân quả (Causal Inference):** Sử dụng Double Machine Learning (DML) để làm sáng tỏ mối quan hệ giữa các chỉ số ESG/Rủi ro ESG và lợi nhuận của doanh nghiệp (hàng tháng/hàng năm).

**Kết quả chính:**

* Các mô hình **Linear/Ridge Regression** cho thấy hiệu suất dự báo ổn định nhất ($R^2 \approx 0.999$).
* Dữ liệu lịch sử giá (đặc biệt là giá trễ và đường trung bình động - MA) đóng vai trò chủ đạo trong dự báo ngắn hạn, trong khi các yếu tố ESG có đóng góp không đáng kể trong khung dự báo giá hàng ngày.
* Tuy nhiên, các yếu tố ESG có tác động đáng kể đến **lợi nhuận dài hạn** của doanh nghiệp.

## 🛠 Công nghệ sử dụng

* **Ngôn ngữ:** Python
* **Nền tảng:** Google Colab
* **Thư viện chính:**
* `yfinance`: Thu thập dữ liệu tài chính.
* `scikit-learn`: Triển khai các mô hình Linear, Ridge, Random Forest, Gradient Boosting.
* `xgboost`: Triển khai XGBoost.
* `shap`: Giải thích tầm quan trọng của các tính năng (Feature Importance).
* `DoubleML`: Thực hiện phân tích nhân quả.



## 📂 Cấu trúc dự án

```text
├── data/               # Dữ liệu tài chính & ESG (cần cấu hình)
├── models/             # Script huấn luyện và đánh giá mô hình
├── notebooks/          # Các file Jupyter Notebook (quy trình EDA, Modeling, Causal Inference)
├── README.md           # Tài liệu dự án
└── requirements.txt    # Các thư viện phụ thuộc

```

## 📊 Kết quả đánh giá mô hình (Tập kiểm thử)

| Mô hình | MAE | MSE | $R^2$ |
| --- | --- | --- | --- |
| Linear Regression | 1.93 | 15.46 | 0.9993 |
| Ridge Regression | 1.93 | 15.46 | 0.9993 |
| Random Forest | 6.27 | 583.35 | 0.9718 |
| Gradient Boosting | 6.09 | 528.93 | 0.9745 |
| XGBoost | 19.21 | 10781.21 | 0.4794 |

## 🚀 Cách chạy dự án

1. Clone repository này về máy.
2. Cài đặt các thư viện cần thiết: `pip install -r requirements.txt`
3. Chạy các notebook trong thư mục `notebooks/` theo thứ tự quy trình đã nêu trong báo cáo.

## 🌐 Demo

Bạn có thể trải nghiệm thử các mô hình tại đây: [Stock Prediction Demo - Hugging Face Space](https://www.google.com/search?q=https://huggingface.co/spaces/changle-2110/Stock-Prediction-Demo)