# Các thuật ngữ Working dir, Staging area, Repository

**1. Working dir**

- chính là thư mục làm việc
- khi file ở trạng thái `modified`, để quay lại các thay đổi trc: `git restore <file>` hoặc `git checkout -- <file>`

**2. Staging area**

- khi sử dụng `git add`, các file đang thay đổi (màu đỏ) ở Working dir sẽ đc add vào Staging area (màu xanh)
- unstage ra khỏi Staging area: `git restore --staged <file>` hoặc `git reset HEAD <file>`

**3. Repository**

3.1 Local repo

- Khi thực hiện commit, những thay đổi ở staging đã được cho vào local repo (lưu 1 tập hợp các commit) và `git status` sẽ trống =)).
