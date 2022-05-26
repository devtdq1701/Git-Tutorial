# git reset (hãy thận trọng khi làm việc với nó =))))

- ngoài mục đích để loại bỏ file ra khỏi stage area thì `git reset` còn dùng để undo commit (quay lại trc commit đó)

- `git reset --soft <commit-id>`: xóa bỏ commit, HEAD trỏ về vào vị trí của commit trc và các thay đổi vẫn còn nằm trong staging area (màu xanh).
- `git reset --mixed <commit-id>`:  tương tự `--soft` nhưng file nằm trong working dir (màu đỏ).
- `git reset --hard <commit-id>`: xóa bỏ hoàn toàn commit cùng những thay đổi.