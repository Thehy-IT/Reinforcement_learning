# Reinforcement Learning - Bài tập thực hành (Labs)

Kho lưu trữ này chứa các bài tập thực hành (Lab 1 và Lab 2) về môn học **Học tăng cường (Reinforcement Learning)**. Các bài lab tập trung vào việc làm quen với môi trường Gymnasium, xây dựng các thuật toán cơ bản từ lập trình động (Dynamic Programming) đến các phương pháp học dựa trên giá trị (Temporal Difference Learning).

---

## Cấu trúc thư mục

- `Lab1.ipynb`: Làm quen với Gymnasium, MDP, Rời rạc hóa trạng thái, Value Iteration và Policy Iteration.
- `Lab2.ipynb`: Cài đặt và so sánh Q-learning (Off-policy) và SARSA (On-policy) trên môi trường FrozenLake.
- `Lab1.pdf` & `Lab2.pdf`: Bản xuất file PDF từ notebook để xem nhanh kết quả.
- `images/` (Các file `.png` trong gốc): Các đồ thị kết quả huấn luyện, so sánh hiệu suất và Heatmap của Q-table.

---

## Chi tiết các bài Lab

### Lab 1: Giới thiệu RL & Lập trình động (MDP)

- **Môi trường:** `CartPole-v1` và `MountainCar-v0`.
- **Nội dung:**
  - Tìm hiểu không gian trạng thái (State Space) và hành động (Action Space).
  - Chạy thử nghiệm với **Random Agent**.
  - **Rời rạc hóa trạng thái (Discretization):** Chuyển đổi không gian trạng thái liên tục của CartPole thành các bins rời rạc để áp dụng các thuật toán bảng (tabular methods).
  - **Model-based RL:** Thu thập dữ liệu để ước lượng ma trận xác suất chuyển trạng thái $P(s'|s,a)$ và hàm phần thưởng $R(s,a)$.
  - **Thuật toán:** Cài đặt **Value Iteration** và **Policy Iteration** để tìm chính sách tối ưu.

### Lab 2: Q-Learning vs SARSA

- **Môi trường:** `FrozenLake-v1` (4x4 và 8x8).
- **Nội dung:**
  - Xây dựng bảng **Q-table** để lưu trữ giá trị hành động.
  - Chiến lược **Epsilon-Greedy** để cân bằng giữa Khám phá (Exploration) và Khai thác (Exploitation).
  - **Q-Learning (Off-policy):** Cập nhật dựa trên giá trị tối ưu của trạng thái kế tiếp.
  - **SARSA (On-policy):** Cập nhật dựa trên hành động thực tế tiếp theo của Agent.
  - **So sánh:** Phân tích sự khác biệt về độ an toàn và tốc độ hội tụ giữa Q-learning và SARSA trong môi trường trơn trượt (slippery).

---

## Kết quả tiêu biểu

Repository bao gồm các kết quả trực quan hóa:

- **`comparison_plot.png`**: So sánh Learning Curve giữa các thuật toán trong Lab 1.
- **`qtable_heatmap.png`**: Biểu đồ nhiệt thể hiện giá trị Q-value cho từng hành động tại mỗi ô trong FrozenLake.
- **`final_benchmark.png`**: Tỉ lệ thắng (Win Rate) sau 30,000 episodes huấn luyện, so sánh giữa Q-learning và SARSA.

---

## Yêu cầu hệ thống

Để chạy các notebook này, bạn cần cài đặt các thư viện sau:

```bash
pip install gymnasium numpy matplotlib
```

Hoặc sử dụng môi trường ảo đã thiết lập sẵn trong thư mục `.venv`.

---

*Thực hiện bởi: Huỳnh Thế Hy*
