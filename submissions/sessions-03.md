# Session 03 - Cryptography & Wallet
- Student: Lê Thị Bích Ngọc
- GitHub:https://github.com/lngoccccccc07000/Sessions-04-Consensus-Blockchain-Architecture/edit/main/submissions/sessions-03.md
- Submitted: 2026-10-11
- Commit:https://github.com/lngoccccccc07000
## 1. Summary
-Hàm băm (hash function) biến dữ liệu có độ dài bất kỳ thành một chuỗi đầu ra có độ dài cố định, gọi là giá trị băm

-Ứng dụng của blockchain ở trong hàm băm:

               +Định danh giao dịch
               
               +Liên kết block
               
               +Cây Merkle
               
               +Proof of Work

 -Blockchain dùng mật mã bất đối xứng: mỗi người dùng sở hữu một cặp khóa gồm khóa bí mật (private key) và khóa công khai (public key)  

 -Chữ ký số (digital signature) chứng minh một giao dịch do đúng chủ sở hữu tạo ra mà không cần tiết lộ khóa bí mật

-Cụm từ khôi phục (seed phrase) là 12 hoặc 24 từ tiếng Anh theo chuẩn BIP-39, dùng để sinh ra toàn bộ khóa của một ví phân cấp xác định (HD wallet).

-Mất cụm từ khôi phục và mất thiết bị đồng nghĩa với mất tài sản vĩnh viễn. Không đội ngũ chính thức nào yêu cầu bạn cung cấp cụm từ này.

 ##2. Topic notes
 
-Hàm băm :là phép biến đổi một chiều: từ dữ liệu tính ra giá trị băm rất nhanh, nhưng từ giá trị băm không thể suy ngược lại dữ liệu gốc

-Tính chất:
<img width="776" height="315" alt="image" src="https://github.com/user-attachments/assets/ed086c9d-4856-458d-b630-232c761d47ca" />

-Ứng dụng :

            +Định danh giao dịch: mỗi giao dịch có một mã băm duy nhất (Transaction ID).
            
            +Liên kết block: mỗi block lưu giá trị băm của block trước, nên sửa một block sẽ làm đứt chuỗi.
            
            +Cây Merkle: tóm tắt hàng nghìn giao dịch thành một giá trị Merkle Root để xác minh nhanh.
            
            +Proof of Work: thợ đào phải tìm giá trị băm thỏa điều kiện độ khó của mạng.

-  Khóa công khai được tính từ khóa bí mật trên đường cong elliptic secp256k1. Ngược lại, từ khóa công khai tìm ra khóa bí mật, là không khả thi về mặt tính toán.

-  Khóa bí mật: Là một số ngẫu nhiên 256 bit, được giữ tuyệt đối bí mật và chỉ thuộc sở hữu của chủ sở hữu (ai nắm giữ khóa này sẽ có toàn quyền với tài sản).

-Quy trình ký và xác minh

            +A tạo giao dịch .
           
            +ví băm nội dung giao dịch.
            
            +Ví ký giá trị băm bằng khóa bí mật của A.
            
            +Giao dịch kèm chữ ký được gửi lên mạng.
            
            + Các node dùng khóa công khai của A để xác minh chữ ký.
            
            +Giao dịch hợp lệ được ghi vào block.

  <img width="804" height="250" alt="image" src="https://github.com/user-attachments/assets/02bffff1-1691-42c9-b9c2-065253b24587" />
  
 -Ví (wallet) không chứa coin. Tài sản được ghi trên blockchain: ví chỉ lưu khóa, hiển thị số dư và ký giao dịch thay người dùng.Địa chỉ ví
  (address) được tạo qua một chuỗi biến đổi một chiều:
        
              +Khóa bí mật: số bí mật 256 bit.
              
              +Khóa công khai: tính từ khóa bí mật trên đường cong secp256k1.
              
              +Giá trị băm: băm khóa công khai để rút gọn.
              
              +Địa chỉ: chuỗi nhận tài sản, có thể chia sẻ công khai.
-Phân biệt ví nóng,lạnh:
<img width="786" height="335" alt="image" src="https://github.com/user-attachments/assets/532f4c3b-fc2d-4244-9c02-6c2c4960db21" />

-So sánh ví lưu lý và tự lưu ký
<img width="793" height="376" alt="image" src="https://github.com/user-attachments/assets/ebbc3384-9e45-4d5d-8006-3cc8d86dee83" />

-6 nguyên tắc bảo mật ví cơ bản:

    + Không chia sẻ cụm từ khôi phục với bất kỳ ai, dưới bất kỳ hình thức nào.
    +Sao lưu cụm từ khôi phục ngoại tuyến (giấy, tấm kim loại), không chụp ảnh hay lưu trên cloud.
    +Kiểm tra kỹ địa chỉ nhận trước khi gửi, đặc biệt các ký tự đầu và cuối.
    +Dùng ví phần cứng cho tài sản giá trị lớn.
    +Cảnh giác lừa đảo: website giả, tin nhắn tự xưng hỗ trợ, airdrop lạ.
    +Gửi thử một giao dịch nhỏ trước khi chuyển số tiền lớn.

           



## 3. Work completed
không có
## 4. Evidence
không có
## 5. Blockers
không có 
## 6. Takeaway
không có
