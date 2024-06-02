# README 파일 작성하기
---
# _1. top 명령어_
```
top [옵션]
```
#### top 명령어는 Linux에서 실행 중인 프로세스에 대한 실시간 보기를 표시하고 커널 관리 작업 을 표시합니다
- 시스템의 **현재 상태**를 실시간으로 모니터링
- CPU, 메모리 사용량 및 각 **프로세스의 상태** 확인
 ![top 명령어](https://github.com/baejongto/20202525BaeJongOk/assets/170800055/034cadb9-736f-492a-b1d5-d0f08a8bf037)
#### top 명령어 표시 항목
| 항목     | 설명 |
|----------|------|
| PID      | 프로세스 ID입니다. 각 프로세스를 식별하는 고유 번호 |
| USER     | 프로세스를 실행한 사용자 |
| PR       | 프로세스의 우선순위 |
| NI       | nice 값으로, 프로세스의 우선순위를 조정하는 데 사용 |
| VIRT     | 프로세스가 사용 중인 가상 메모리 양 |
| RES      | 프로세스가 사용 중인 실제 메모리 양 |
| SHR      | 프로세스가 사용 중인 공유 메모리 양 |
| S        | 프로세스의 상태 |
| %CPU     | 프로세스가 사용하는 CPU 시간의 비율 |
| %MEM     | 프로세스가 사용하는 물리적 메모리의 비율 |
| TIME+    | 프로세스가 사용한 총 CPU 시간 |
| COMMAND  | 실행 중인 명령어 이름 또는 경로 |

#### top 명령어 주요 옵션
| 옵션 | 설명 |
|------|------|
| `-d` | 화면 갱신 주기를 설정합니다. 기본값은 3초 |
| `-p` | 특정 PID의 프로세스만 모니터링 |
| `-u` | 특정 사용자의 프로세스만 모니터링 |
| `-n` | 지정한 횟수만큼 갱신을 반복 후 종료 |


---
# _2. ps 명령어_
```
ps [옵션]
```
#### ps 명령어는 현재 실행 중인 프로세스와 상태를 출력하는 명령어입니다.
1. 현재 실행 중인 **프로세스 정보**를 출력하는 명령어.
2. **프로세스 ID(PID), 사용자, CPU 및 메모리 사용량** 등을 확인.
![스크린샷 2024-06-02 211945](https://github.com/baejongto/20202525BaeJongOk/assets/170800055/7a31fe05-051b-49a8-ba30-ddfc12fe1287)
![스크린샷 2024-06-02 211853](https://github.com/baejongto/20202525BaeJongOk/assets/170800055/dc70d1ff-97c6-4430-be07-7402ebb9df30)
#### ps 명령어 주요 옵션
| 옵션 | 설명 |
|------|------|
| `-e` | 모든 프로세스 출력 |
| `-f` | 풀 포맷 출력 |
| `-u` | 특정 사용자 소유의 프로세스 출력 |
---
# _3. jobs 명령어_
```
jobs [옵션]
```
#### jobs명령어는 실행 중인 작업들을 보여줍니다.
![jobs](https://github.com/baejongto/20202525BaeJongOk/assets/170800055/9ee36319-7d5a-459b-95fc-5262a2b82504)
![jobs2](https://github.com/baejongto/20202525BaeJongOk/assets/170800055/bea44572-650a-4378-951e-a1b371ddee9b)

#### jobs 명령어 주요 옵션

| 옵션 | 설명 |
|------|------|
| `-p` | 백그라운드에 있는 프로세스의 프로세스 아이디(PID)만 출력 |
| `-l` | 백그라운드에 있는 프로세스의 프로세스 아이디(PID)를 함께 출력 |
| `-s` | 백그라운드에 있는 프로세스 중 멈춰있는 프로세스만 출력 |
| `-r` | 백그라운드에 있는 프로세스 중 실행 중인 프로세스만 출력 |

---
# _4. kill 명령어_
```
kill [옵션] [pid]
```
#### ps명령어는 프로세스에 시그널을 보내는 명령어입니다.
- ps명령어를 통해 프로세스 작업을 종료시킬 수 있다.
- **jobs -l** 을 통해 백그라운드에 있는 프로세스의 **pid를 본후 kill** 할 수 있다.
- 아래 그림은 vi를 cirl+z로 일시 중지 후 kill 한 모습
![kill](https://github.com/baejongto/20202525BaeJongOk/assets/170800055/882f694e-6641-4bab-b7f9-6fe7e7c247fd)
#### kill 명령어 주요 옵션
| 옵션 | 설명 |
|------|------|
| `-9`  | 강제 종료 |
| `-15` | 정상 종료 |
