## 🗂️ 1. 파일 및 디렉터리 관리

| 명령어             | 설명                  | 예시                                          |
| --------------- | ------------------- | ------------------------------------------- |
| `ls`            | 현재 디렉터리의 파일 목록 출력   | `ls -l`, `ls -a`                            |
| `cd`            | 디렉터리 이동             | `cd /home/user`, `cd ..`                    |
| `pwd`           | 현재 디렉터리 경로 출력       | `pwd`                                       |
| `mkdir`         | 새 디렉터리 생성           | `mkdir project`                             |
| `rmdir`         | 비어있는 디렉터리 삭제        | `rmdir old_folder`                          |
| `rm`            | 파일 또는 디렉터리 삭제       | `rm file.txt`, `rm -r folder`               |
| `cp`            | 파일 또는 디렉터리 복사       | `cp file1 file2`, `cp -r dir1 dir2`         |
| `mv`            | 파일 이동 또는 이름 변경      | `mv old.txt new.txt`, `mv file /home/user/` |
| `touch`         | 빈 파일 생성 또는 수정 시간 변경 | `touch new.txt`                             |
| `cat`           | 파일 내용 출력            | `cat file.txt`                              |
| `more` / `less` | 긴 파일 내용 페이지 단위로 보기  | `less log.txt`                              |
| `head` / `tail` | 파일의 앞/뒤 일부만 출력      | `head -n 10 file.txt`, `tail -f log.txt`    |

---

## 📦 2. 파일 검색 및 탐색

| 명령어       | 설명                | 예시                         |
| --------- | ----------------- | -------------------------- |
| `find`    | 조건에 맞는 파일 검색      | `find . -name "*.txt"`     |
| `grep`    | 파일 내 문자열 검색       | `grep "error" logfile.txt` |
| `locate`  | 인덱스를 이용해 빠른 파일 검색 | `locate config.json`       |
| `which`   | 실행 파일의 절대 경로 출력   | `which python`             |
| `whereis` | 명령어의 관련 파일 위치 확인  | `whereis gcc`              |

---

## ⚙️ 3. 시스템 및 사용자 정보

| 명령어        | 설명                       | 예시         |
| ---------- | ------------------------ | ---------- |
| `whoami`   | 현재 로그인한 사용자 확인           | `whoami`   |
| `id`       | 사용자와 그룹 ID 출력            | `id user`  |
| `uname`    | 시스템 정보 출력                | `uname -a` |
| `hostname` | 호스트 이름 확인                | `hostname` |
| `top`      | 실시간 프로세스 및 메모리 사용량 보기    | `top`      |
| `htop`     | 인터랙티브 프로세스 모니터링 (패키지 필요) | `htop`     |
| `df`       | 디스크 사용량 확인               | `df -h`    |
| `du`       | 디렉터리별 용량 확인              | `du -sh *` |
| `free`     | 메모리 사용량 출력               | `free -h`  |
| `date`     | 시스템 날짜 및 시간 표시           | `date`     |
| `uptime`   | 시스템 가동 시간 및 부하 표시        | `uptime`   |

---

## 🔐 4. 권한 및 사용자 관리

| 명령어                   | 설명             | 예시                                             |
| --------------------- | -------------- | ---------------------------------------------- |
| `chmod`               | 파일 권한 변경       | `chmod 755 script.sh`                          |
| `chown`               | 파일 소유자 변경      | `chown user:group file.txt`                    |
| `sudo`                | 관리자 권한으로 명령 실행 | `sudo apt update`                              |
| `passwd`              | 사용자 비밀번호 변경    | `passwd`                                       |
| `adduser` / `userdel` | 사용자 추가 / 삭제    | `sudo adduser newuser`, `sudo userdel olduser` |

---

## 🧮 5. 프로세스 제어

| 명령어         | 설명                  | 예시                          |
| ----------- | ------------------- | --------------------------- |
| `ps`        | 현재 실행 중인 프로세스 확인    | `ps aux`                    |
| `kill`      | 특정 프로세스 종료          | `kill 1234`, `kill -9 1234` |
| `jobs`      | 백그라운드 작업 목록         | `jobs`                      |
| `fg` / `bg` | 포그라운드 / 백그라운드로 전환   | `fg %1`, `bg %2`            |
| `nohup`     | 로그아웃 후에도 프로세스 유지 실행 | `nohup python script.py &`  |

---

## 🌐 6. 네트워크 관련

| 명령어                    | 설명                | 예시                                     |
| ---------------------- | ----------------- | -------------------------------------- |
| `ping`                 | 네트워크 연결 테스트       | `ping google.com`                      |
| `curl`                 | URL 요청 및 데이터 다운로드 | `curl -O https://example.com/file.zip` |
| `wget`                 | 파일 다운로드           | `wget https://example.com/file.zip`    |
| `ifconfig` / `ip addr` | 네트워크 인터페이스 정보     | `ip addr show`                         |
| `netstat`              | 네트워크 연결 상태 확인     | `netstat -tuln`                        |
| `scp`                  | 원격 서버 간 파일 복사     | `scp file user@server:/path`           |
| `ssh`                  | 원격 접속             | `ssh user@server`                      |

---

## 📑 7. 압축 및 아카이브

| 명령어               | 설명            | 예시                                                  |
| ----------------- | ------------- | --------------------------------------------------- |
| `tar`             | 파일 압축/해제      | `tar -cvf archive.tar dir/`, `tar -xvf archive.tar` |
| `gzip` / `gunzip` | 단일 파일 압축 / 해제 | `gzip file.txt`, `gunzip file.txt.gz`               |
| `zip` / `unzip`   | ZIP 압축 / 해제   | `zip -r archive.zip folder/`, `unzip archive.zip`   |

---

## 🧰 8. 패키지 관리 (예: Ubuntu 기준)

| 명령어           | 설명           | 예시                         |
| ------------- | ------------ | -------------------------- |
| `apt update`  | 패키지 목록 갱신    | `sudo apt update`          |
| `apt install` | 패키지 설치       | `sudo apt install python3` |
| `apt remove`  | 패키지 제거       | `sudo apt remove vim`      |
| `apt upgrade` | 설치된 패키지 업데이트 | `sudo apt upgrade`         |

---

## 📜 9. 기타 유용한 명령어

| 명령어       | 설명         | 예시                   |
| --------- | ---------- | -------------------- |
| `echo`    | 텍스트 출력     | `echo "Hello Linux"` |
| `history` | 명령어 기록 보기  | `history`            |
| `alias`   | 명령어 단축어 설정 | `alias ll='ls -la'`  |
| `clear`   | 터미널 화면 지우기 | `clear`              |
| `exit`    | 터미널 종료     | `exit`               |
