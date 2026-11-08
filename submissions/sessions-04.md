# Session 04 - Consensus & Blockchain Architecture
- Student: Lê Thị Bích Ngọc
- GitHub:https://github.com/lngoccccccc07000/Sessions-04-Consensus-Blockchain-Architecture
- Submitted: 2026-08-11
- Commit:https://github.com/lngoccccccc07000
## 1. Summary
-Cơ chế đồng thuận (consensus mechanism) là cách các node trong mạng thống nhất một trạng thái chung của sổ cái, kể cả khi có node bị lỗi hoặc cố tình gian lận.  Đây là lời giải cho bài toán các vị tướng Byzantine.

-Proof of Work (bằng chứng công việc) là cơ chế cạnh tranh bằng năng lực tính toán.

-Proof of Stake (bằng chứng cổ phần) bảo đảm an ninh bằng tài sản ký quỹ .

-Tính chung cuộc (finality) là thời điểm một giao dịch không thể bị đảo ngược nữa. Giao dịch vừa vào block chưa chắc chắn tuyệt đối; số xác nhận cần chờ phụ thuộc giá trị giao dịch và cơ chế đồng thuận.

-Có 2 cách biểu diễn tài sản chính:
               +mô hình tài khoản (account-based).
   
              +mô hình đầu ra chưa tiêu (UTXO, Unspent Transaction Output).


 ##2. Topic notes
-Proof of Work: Thợ đào lặp lại vòng: thử nonce, băm block, so với ngưỡng mục tiêu (target), rồi thử lại. Ai tìm được giá trị băm nhỏ hơn ngưỡng trước sẽ thêm block và nhận phần thưởng.

-Proof of Stake:  Người xác thực (validator) khóa coin làm tài sản đảm bảo:
   +Người xác thực được chọn để đề xuất block.
   +Những người xác thực khác kiểm tra block.
   +Người xác thực gian lận bị cắt một phần coin đã khóa (slashing).
-So sánh:<img width="973" height="459" alt="image" src="https://github.com/user-attachments/assets/14e6bcd2-8d88-4cf4-a7b8-6462ef798eee" />

-Finality dược chia làm 2 loại:

<img width="978" height="362" alt="image" src="https://github.com/user-attachments/assets/5631cd84-0848-407c-be2e-26aa0261f82e" />






## 3. Work completed
không có 
## 4. Evidence
không có
## 5. Blockers
không có 
## 6. Takeaway
không có
