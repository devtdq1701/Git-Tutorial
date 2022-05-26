**1. git init**

- tạo ra thư mục `.git` bên trong thư mục của project (tạo ra local repo)
- `.git` lưu thông tin lịch sử của project

**2. git status**

- tracking thay đổi (trạng thái) của các file trong project (thực tế là trong working directory và staging area)
  ![](imgs/git-status.png)

Giải thích:

- On branch master: đang ở nhánh master (đừng quan tâm nó là gì, mình sẽ giải thích ở bài tiếp theo)
- No commits yet: chưa có commit (danh từ) nào cả
- Untracked files: có file chưa đc track, cần được `git add` để gộp vào những cái sẽ commit (động từ).

**3. git add**

- Đưa những những thay đổi sang staging area
- Sau khi sử dụng `git add`, cùng check lại bằng `git status`:
  ![](<imgs/git-add(1).png>)
  ![](<imgs/git-add(2).png>)
  - file mới thêm vào sẽ chuyển từ màu đỏ(untracked) sang xanh (new file)
  - file ở trạng thái `modified` (màu đỏ) sang `modified` (màu xanh)
  - add tất cả những thay đổi: `git add .`

**4. git commit**

- đóng gói những thay đổi (màu xanh lá cây) mà bạn đã `git add` thành 1 `object` và dán cho nó 1 `id`
- sử dụng tham số `-m` để viết 1 Messages nhằm mục đích note lại commit này đã làm gì nhằm mục đích cho mình cũng như ng khác hiểu mình đã commit cái gì. Quy chuẩn: ngắn gọn (ít hơn 50 ký tự), viết hoa chữ cái đầu, không kết thúc = dấu .
  ![](imgs/git-commit.png)
  Trong đó: - `727f355`: commit id - 2 file changed, 17 insertion+: 2 file đã thay đổi, trong đó có 17 thêm mới
- Nếu cài git lần đầu, bạn sẽ chưa đc commit mà sẽ nhận được thông báo có dạng như sau:
  ![](imgs/first-git-notify.png)

=> hãy thực hiện cấu hình:

```
git config --global user.name "<your_username_here>"
git config --global user.email "<your_gmail_here>"
git config --list
```

- check lại bằng `git status`:
  ![](<imgs/git-status(2).png>)

  - working tree clean: mình sẽ giải thích trong bài học sau.

- thay đổi note của commit gần nhất
  ```
  git commit --amend -m "amend description message"
  ```
