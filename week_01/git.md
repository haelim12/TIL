# ๐พ git ์ ๋ฆฌ

- ์ ์ฅ์ ์์ฑ
    $ git init : git ์ ์ฅ์ ๋ง๋ค๊ณ  ๊ด๋ฆฌ

- ๋ฒ์  ๊ด๋ฆฌ

    1. ์์์ ํ๊ณ 
    2. ๋ณ๊ฒฝ๋ ํ์ผ์ ๋ชจ์ (add)
    3. ๋ฒ์ ์ผ๋ก ๋จ๊ธด๋ค (commit)

## git ๊ธฐ์ด ๋ช๋ น์ด

### $ git add <file>
- working directory ์์ ๋ณ๊ฒฝ๋ด์ฉ์ staging area์ ์ถ๊ฐํ๊ธฐ ์ํด ์ฌ์ฉ

### git commit -m'<์ปค๋ฐ๋ฉ์ธ์ง>'
- staged ์ํ์ ํ์ผ์ ์ปค๋ฐ์ ํตํด ๋ฒ์ ์ผ๋ก ๊ธฐ๋ก

### git status
-  ํ์ฌ ํ์ผ ์ํ

### git log
- ํ์ฌ ์ ์ฅ์์ ๊ธฐ๋ก๋ ์ปค๋ฐ ์กฐํ
    - $ git log -1 : ์ต๊ทผ 1๊ฐ
    - $ git log --oneline : ํ์ค๋ก

## git ์ํฉ๋ค
- (1ํต) Untracted Files : 1.txt๋ฅผ ๋ง๋ค์์ง๋ง, add๋ฅผ ํ์ง ์์
- (2ํต) Changed to be commited : ๋ณด๊ณ ์.txt๋ฅผ ๋ง๋ค๊ณ  addํจ
- nothing to commit, working tree clean : ๋ชจ๋ add, commit,ํ ์ดํ => 1ํต, 2ํต ๋น์ด์์
- Changes not staged for commit : ์ปค๋ฐ๋ ์  ์๋ ๋ณด๊ณ ์.txt ํ์ผ์ ์์ ํ ์ํ


> ์ ๋ฆฌ

git init

git add
