考试范围
BFD 全部vl

MCI 最后一个不考

# 2.2.2024

## Wanjin
BFD: 
- [x] VL 5 XML
- [x] VL 6 Grafiken
- [x] Übung 123

## Jingting
- [x] MCI 6.Vorlesung
- [x] BFD VL 4 Multimedia

## Xin
- [x] BFD: VL 7: PDF

# Git 常规流程
如果其他人已经在远程仓库进行了修改，而你本地也有一些修改需要提交，你需要先将远程仓库的最新修改拉取到本地，然后再将你的修改推送到远程仓库。以下是一般的步骤：
1. **拉取远程仓库的最新修改：**
    `git pull origin master`
    这里假设你想要拉取 `master` 分支的最新修改。如果你在其他分支上工作，将 `master` 替换为你当前工作的分支名。
    
    如果有冲突，Git 会尝试自动合并，但如果无法自动合并，你需要手动解决冲突。
    
2. **解决冲突（如果有的话）：** 如果 `git pull` 之后提示有冲突，你需要打开相关文件，手动解决冲突。解决完冲突后，运行以下命令继续合并：
    
    `git add . git commit -m "解决冲突并合并远程修改"`
    
3. **推送本地修改到远程仓库：**
    
    `git push origin master`
    
    这里同样假设你要推送到 `master` 分支。替换为你当前工作的分支名。
    
    如果其他人在你拉取远程修改之后已经推送了新的修改，可能会发生推送失败的情况。这时你需要再次执行 `git pull` 操作，解决任何可能的冲突，然后才能成功推送。

# Wanjin BFD Nachverbessern Plan
- [x] **VL 1**: 2h 40 min
- [ ] **VL 2**: 4h
- [ ] **VL 3**: 1.5h
**VL 4**: 3h
**VL 5**: 0
**VL 6**: 3h
**VL 7**: 1.5h





