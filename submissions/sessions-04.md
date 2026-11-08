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

-Một blockchain khó đạt được cùng lúc cả ba mục tiêu: phi tập trung, bảo mật và khả năng mở rộng.Chúng hay còn được gọi là bộ ba bất khả thi. Tăng một mục tiêu thường phải hy sinh một mục tiêu khác, và đây là lý do Layer 2 ra đời

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

-Vai trò của từng Layer 1,2:
<img width="982" height="303" alt="image" src="https://github.com/user-attachments/assets/340897c4-0267-44fb-b659-0cd94bd53a4b" />

-Layer 1 là đường cao tốc chính, còn Layer 2 là đường gom: xử lý bớt lượng xe rồi đưa kết quả nhập về cao tốc.

-Phân biệt mô hình tài khoản và mô hình UTXO

<img width="991" height="496" alt="image" src="https://github.com/user-attachments/assets/48231bdc-3fa5-4197-b608-10c7c36fd222" />

-Các mô hình triển khai blockchain và sự khác biệt giữa chúng:
<img width="982" height="516" alt="image" src="https://github.com/user-attachments/assets/29d7f275-8a22-4d44-bda6-643f9d5a3fdc" />

-Tình huống: hệ thống cấp bằng đại học.
Các trường đại học muốn cấp và thu hồi bằng trên blockchain. Kiến trúc đề xuất gồm ba bước:

         +Các trường lập liên minh.
         
         +Liên minh vận hành một blockchain cấp phép để cấp và thu hồi bằng.
         
         +Định kỳ neo giá trị Merkle Root của dữ liệu lên blockchain công khai.


## 3. Work completed
Bài 1:
<img width="1919" height="639" alt="image" src="https://github.com/user-attachments/assets/8b57a211-9ee5-4b3c-9fe8-35a5d0fbb6e9" />
<img width="1917" height="498" alt="image" src="https://github.com/user-attachments/assets/0c364e82-c788-41e2-88eb-f36f6be36830" />

-Mã Hash của Block 1 thay đổi khiến cho mã Hash của Block 2 và Block 3 không còn khớp nữa từ đó làm hỏng toàn bộ  liên kết của các chuỗi phía sau. Đây chính là minh họa cho tính bất biến và cơ chế bảo mật của blockchain.

Bài 2:
<img width="1891" height="904" alt="image" src="https://github.com/user-attachments/assets/def9bfbd-0b21-487f-bbd5-c432ae71c99c" />
<img width="1497" height="313" alt="image" src="https://github.com/user-attachments/assets/c84b5867-fdb0-4db1-adf4-23ffe94a33ec" />


Mã giao dịch :6ff0fbfffcb337b33149186eb7d2c63fbe6d5de4e878a0f6ebdda685915550af

Số xác nhận:1 xác nhận

Input:bc1q5mqy8a6d3wjwh9ghxunernnmpqu454qq4e4ac

Output: 

        + bc1qtcfxnfphx359kmsqxzeqyup6meqeh3gh8jf

        + bc1q5mqy8a6d3wjwh9ghxunernnmpqu454qq4e

Bài 3:
<img width="1906" height="916" alt="image" src="https://github.com/user-attachments/assets/9c6323e9-3c10-476b-bc05-4775cc1f554a" />
-Tên dự án:Base Chain

-Loại công nghệ:Optimistic Rollup

-Layer 1:Etherum
        
## 4. Evidence
không có
## 5. Blockers
không có 
## 6. Takeaway
không có
