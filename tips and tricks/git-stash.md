# git stash

```

➜ vi-du git:(dev) ✗ git add a.txt
➜ vi-du git:(dev) ✗ git commit -m "change a.txt"
[dev 18ee47c] change a.txt
1 file changed, 2 insertions(+)
➜ vi-du git:(dev) vim a.txt
➜ vi-du git:(dev) ✗ git checkout main
error: Your local changes to the following files would be overwritten by checkout:
a.txt
Please commit your changes or stash them before you switch branches.
Aborting

```

Trường hợp: Bạn đang ở ngay giữa task và có khá nhiều file changed trên branch **dev** thì leader báo "code của chú trên branch **production** đang có bug, quay lại hot fix cho anh luôn nhé!". Để giải quyết vấn đề, bạn cần checkout sang branch **production**. Thông thường, sẽ có 2 lựa chọn:

- Chạy git reset --hard để loại bỏ những thay đổi đã được commit của bạn.
- Ghi lại công việc chưa hoàn tất của bạn như là một commit mới.

Tùy chọn đầu tiên làm mất tất cả công việc của bạn, trong khi cái sau dẫn đến một phần commit không có ý nghĩa. Không có tình huống là được mong đợi cả.

Đây là lúc lệnh `git stash` phát huy tác dụng của nó. Hãy tưởng tượng nó giống như `git reset --hard`, nó cung cấp cho bạn một branch sạch sẽ, nhưng nó cũng ghi lại các thay đổi không đầy đủ bên trong. Sau khi khắc phục xong lỗi nghiêm trọng, bạn có thể tái áp dụng những thay đổi này và bắt đầu lại từ nơi bạn đang dở dang. Bạn có thể xem `git stash` như một nút "tạm dừng" cho tiến trình công việc của bạn.

Dưới đây là những điều hữu ích mà git stash có:

- Git stash save
- Git stash list
- Git stash apply
- Git stash pop
- Git stash show
- Git stash branch <name>
- Git stash clear
- Git stash drop

1. git stash save

- giống như `git stash` nhưng có thêm option.
- dùng để lưu tạm lại trạng thái làm việc hiện tại trên current branch bằng cách tạo ra các stash,

- Git stash cùng mới một message kèm theo

```

git stash save "Toi dang Code cai gi the nay"

```

Git stash loại bỏ những files không được theo dõi

```

git stash save -u

```

or

```

git stash save --include-untracked

```

2. Git stash list

xem danh sách stash:

```

git stash list

```

output:

```

stash@{0}: WIP on master: 4e22905 abc 1865891265912
stash@{1}: On master: Toi dang Code cai gi the nay
(END)

```

Đây là danh sách các stashes mà bạn tạo ra, và cái gần nhất bạn tạo nó ở trên đầu.

3. git stash apply

Lệnh này cơ bản là sẽ lấy stash cuối cùng (gần nhất) để apply vào code:

```

git stash apply

```

Thế nếu giờ mà bạn muốn apply một thằng khác thì thế nào nhỉ? đơn giản lắm lấy thằng id của stash đó ra thôi chứ sao

```

git stash apply stash@{1}

```

4. git stash pop

Tương tự như `git stash apply` nhưng nó sẽ xoá stash đó khỏi đống stash

```

➜ leuleu git:(master) git stash pop
On branch master
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)

    modified:   helloworld.js

no changes added to commit (use "git add" and/or "git commit -a")
Dropped refs/stash@{0} (f86f17ccf69028ed447c7b59bae6782d1ff33b24)

```

Tương tự như **apply** nó cũng lôi thằng gần nhất ra, và bạn muốn nó lôi thằng nào ra thì thêm id của nó vào sau nhé

```

git stash pop stash@{1}

```
