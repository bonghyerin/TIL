### **로컬 저장소에 파일을 commit**

### add → commit

init - touch - status - add - commit - log

- 로컬 저장소 초기화

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice
$ git init
Initialized empty Git repository in C:/Users/SSAFY/Desktop/git-practice/.git/
```

- 텍스트 파일 생성

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ touch 01.txt
```

- 현재 로컬 저장소의 파일 상태 확인 (git의 상태를 확인)

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        01.txt

nothing added to commit but untracked files present (use "git add" to track)
```

- 현재 디렉토리에 있는 모든 디렉토리가 한 번에 staging area에 add

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git add .
```

- staging area에 있는 파일들을 저장소에 기록 (commit 생성)

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git commit -m "first commit"
[master (root-commit) 0658fda] first commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 01.txt
```

- commit 목록 확인

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git log
commit 0658fda4df5db1bc1976953af6e1b2d447745a84 (HEAD -> master)
Author: votreregard <votreregard@naver.com>
Date:   Thu Jan 16 16:58:04 2025 +0900

    first commit
```

- 두번째 텍스트 파일 생성

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ touch 02.txt
```

- 현재 로컬 저장소의 파일 상태 확인 (git의 상태 확인)

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git status
On branch master
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        02.txt

nothing added to commit but untracked files present (use "git add" to track)
```

- 현재 디렉토리에 있는 모든 디렉토리를 저장소에 기록

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git add .
```

- staging area에 있는 파일들을 저장소에 기록 (commit 생성)

```bash
SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
$ git commit -m "second commit"
[master 8b69eb9] second commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 02.txt
```

- commit 목록 확인 : 처음에 commit된 파일이 아래에 위치
  
  
  
```bash
  SSAFY@2□□099 MINGW64 ~/Desktop/git-practice (master)
  $ git log
  commit 8b69eb9a39cb0c9002bfa90a832b6338452972a9 (HEAD -> master)
  Author: votreregard <votreregard@naver.com>
  Date: Thu Jan 16 16:58:54 2025 +0900
   second commit
  commit 0658fda4df5db1bc1976953af6e1b2d447745a84
  Author: votreregard <votreregard@naver.com>
  Date: Thu Jan 16 16:58:04 2025 +0900
   first commit
  ```
  
  
