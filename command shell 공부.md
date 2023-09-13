# command shell 공부
### Command shell의 종류
유닉스 - Bourne Shell, Bash,  fish, zsh 
리눅스 - 유닉스 shell 사용 가능 (Mac OS 도 사용 가능!)
윈도우 - WSL(Windows Subsystem for Linux)을 통해 리눅스를 사용할 수 있기 때문에 위의 shell 사용 가능, Native Terminal 로는 CMD.exe 와 PowerShell 이 있다.


### 백엔드 엔지니어가 쉘 커맨드를 사용하는 경우
* 다른 원격에 있는 서버에 접속한다든지
* 문제있는 버그를 디버깅 하는 경우(해보지 않음)
* 자동화를 위해서 스크립트를 작성하는 경우(해보지 않음)
* 깃 - 버전관리


### 15가지 shell 커맨드
1. 메뉴얼 확인하기  `man`
ex) `man clear` `man pwd` 등등

2. working directory 출력  `pwd` 

3. 파일 목록 `ls`
	- `ls -l`  long format option
	- `ls -a`  show hidden format

4. 터미널 출력 항목 지우기 `clear`

5. 현재 경로의 디렉토리 열기 `open .`

6. 경로 변경 `cd`
	* .   현재 경로
	* ..  상위 경로
	* ~  홈 디렉토리
	* -   이전 경로

7.  `find`
```
find . -type file -name "*.txt"
find . -type file -name "*.json"
find . -type directory -name "*2"
```

8. 사용하고자 하는 프로그램의 실행 경로 찾기  `which`
```
which node
which code 
```

9. 새로운 파일 만들거나 기존 파일 날짜 업데이트 `touch`
```
touch new_file1.txt
touch new_file2.txt
```

10. 파일 안의 내용 빠르게 확인하기 `cat`
```
cat new_file1.txt new_file2.txt
```

11. 파일을 만들고 컨텐츠로 넣어주기(덮어쓰거나 추가)  `echo`
```
echo “hello world” > new_file3.txt
echo "Goodbye world" >> new_file3.txt
```

12. 파일, 디렉토리 생성, 이동, 복사, 삭제
```
mkdir -p dir1/subdir1/subdir2 
cp [파일이름] [경로]
mv [파일이름] [경로]
rm [파일이름]
rm -r [폴더이름] // recursive
```

13. global regular expression `grep`
```
grep "world" *.txt
grep -n "world" *.txt // 몇번 째 줄에 있는지 
grep -i "world" *.txt // 대소문자 상관없이 insensitive
grep -r "world" . // 현재경로와 그 하위 경로 모두를 찾는다
```

14. 환경 변수 설정 `export`
```
export MY_DIR="dir1"
```
	* 환경 변수 출력 `env`
	* 환경 변수 사용시 `$`
	* 환경 변수 해제 `unset`







