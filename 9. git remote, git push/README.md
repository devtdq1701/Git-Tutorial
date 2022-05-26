## git remote

- connect local repo đến 1 remote repo

```
git remote add <remote-name> <server>
```

- list các remote repo đang connect

```
git remote -v
```

- rename remote

```
git remote rename <old> <new>
```

- xóa remote

```
git remote remove <name>
```

## git push

push và merge các thay đổi từ một branch đến một remote & branch.

```
# Push và merge các thay đổi từ một repo local đến một
# remote có tên là "origin" và nhánh "master".
# git push <remote> <branch>
# git push => mặc định ẩn đến => git push origin master
$ git push origin master

# Để connect đến một branch local với một branch remote, thêm vào flag -u:
$ git push -u origin master
# Từ lúc này, bất cứ khi nào bạn muốn push từ cùng một nhánh local đó, sử dụng short-hand:
$ git push
```
