# Bài 6: Ứng dụng AI trong khắc phục lỗi Git Permission Denied

## 1. Sử dụng Prompt AI 3 thành phần

**Công thức:** Vai trò + Bối cảnh + Yêu cầu.

Prompt sử dụng:

```text
Bạn là chuyên viên hỗ trợ kỹ thuật IT.

Tôi đang sử dụng Git trên Windows để đẩy code lên GitHub
nhưng gặp lỗi:
error: open(".git/FETCH_HEAD"): Permission denied.

Hãy giải thích nguyên nhân bằng ngôn ngữ đơn giản
và hướng dẫn cách khắc phục an toàn cho người mới học Git.
```

**Kết quả:** Git không có quyền truy cập hoặc chỉnh sửa file `FETCH_HEAD` trong thư mục `.git`.

## 2. Phân tích và khắc phục lỗi

Không sử dụng Run as Administrator một cách tùy tiện vì có thể làm thay đổi quyền sở hữu file.

Các bước kiểm tra:

1. Đóng các cửa sổ Terminal đang sử dụng Git.
2. Kiểm tra xem có chương trình nào đang sử dụng file trong thư mục `.git` không.
3. Kiểm tra quyền truy cập của thư mục dự án.
4. Mở lại Terminal bằng tài khoản Windows thông thường.
5. Thử kiểm tra:

```bash
git status
```

**Ảnh minh họa:** Chụp màn hình thông báo lỗi và quá trình kiểm tra quyền truy cập. Che thông tin cá nhân và Token.

## 3. Báo cáo lỗi cho giảng viên

Nếu vẫn không khắc phục được, em gửi tin nhắn:

```text
Em chào thầy/cô!

Em gặp lỗi khi đẩy code lên GitHub:

- Môi trường: Windows, PowerShell, Git.
- Lỗi: error: open(".git/FETCH_HEAD"): Permission denied.
- Cách tái hiện: Thực hiện lệnh git push.
- Đã thử: Khởi động lại Terminal và kiểm tra quyền truy cập thư mục.
- Kết quả: Lỗi vẫn chưa được khắc phục.
- Mong muốn: Đẩy code lên GitHub thành công.

Em có đính kèm ảnh chụp màn hình.
Mong thầy/cô hướng dẫn em cách xử lý.

Em cảm ơn thầy/cô!
```
