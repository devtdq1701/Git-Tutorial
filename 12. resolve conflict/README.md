// Resolve conflicts
When will conflicts happen?

1. Changing the same file + same line
2. A deleted fille X, B modified file X

- Method1:
  1. Using `git rebase`
  2. Resolve conflict
  3. Push again with -f
- Method2:
  1. Merge updated master to feature branch
  2. Resolve conflict
  3. Commit and push

## Resolve conflict sử dụng rebase

VD: ô A và B code trên 2 feature branch khác nhau nhưng lại cùng chỉnh sửa 1 file trên cùng 1 số dòng. Sau đó có 2 pull request đồng thời mở. 1 pull request được merge trc và pull request sau sẽ xảy ra hiện tượng conflict
![](imgs/conflict-1.png) ![](imgs/conflict-2.png) ![](imgs/conflict-3.png)

- quy tắc: conflict trên branch nào thì chủ branch đó sẽ đi fix (trong ví dụ này là `feature/resolve-using-rebase-2`).
- checkout sang feature/resolve-using-rebase-2:
