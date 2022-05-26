## git clone

- copy nguyên bản remote repo về máy

```
git clone <remote-url>
```

## git fetch

- fetch những commit không tồn tại trên local từ remote.

```
git fetch <remote> <branch>
```

## git pull

- Pull về từ một repo và merge nó vào branch

```
# git pull <remote> <branch>
# git pull => hoàn toàn mặc định như => git pull origin master
$ git pull origin master

# Merge các thay đổi từ remote branch và rebase
# các commit trong branch lên trên local repo, như sau: "git pull <remote> <branch>, git rebase <branch>"
$ git pull origin master --rebase
```
