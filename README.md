# Open_sw_homework 20243123-이재환
## TOP
* top : 리눅스에서 실시간으로 시스템의 성능을 모니터링하는 도구
---
이 명령어를 통해 CPU 사용량, 메모리 사용량, 실행 중인 프로세스 등의 정보를 확인할 수 있다.(아래사진은 그 예시이다)
![top](https://github.com/hwanlee0321/Open_sw_homework/blob/main/top.png)
* 기본 화면 설명:

첫 줄: 현재 시간, 시스템 가동 시간, 사용자 수, 시스템 부하 평균(load average).


두 번째 줄: 프로세스의 총 수, 실행 중인 프로세스, 중지된 프로세스, 좀비 프로세스.


세 번째 줄: CPU 사용량 (사용자, 시스템, 나이스, 아이들, IO 대기, 하드웨어 인터럽트, 소프트웨어 인터럽트, 스틸).


네 번째 줄: 메모리 사용량 (총 메모리, 사용 중인 메모리, 사용 가능한 메모리, 버퍼/캐시).


다섯 번째 줄: 스왑 사용량 (총 스왑 메모리, 사용 중인 스왑, 사용 가능한 스왑, 버퍼/캐시).

## PS
* ps : 이 명령어는 리눅스에서 현재 실행 중인 프로세스를 확인하는 도구
---
이 명령어는 리눅스에서 현재 실행 중인 프로세스를 확인하는 데 사용된다. (아래사진은 그 예시이다)

대표적으로 사용되는 '$ ps aux'만 알아보자.

ps aux는 모든 프로세스를 확인하는 명령어이다.

(아래사진은 그 예시이다)

![ps](https://github.com/hwanlee0321/Open_sw_homework/blob/main/ps.png)

## JOBS
* jobs : 리눅스에서 현재 쉘 세션에서 실행 중인 작업(job) 목록을 표시하는 도
---
jobs 명령어는 리눅스에서 현재 쉘 세션에서 실행 중인 작업(job) 목록을 표시하는 데 사용된다.

작업은 백그라운드에서 실행 중인 명령어 또는 중지된 명령어를 의미한다.

이 명령어는 사용자가 현재 쉘에서 어떤 작업이 실행 중인지 쉽게 확인할 수 있도록 도와준다.

## KILL
* kill :  리눅스에서 프로세스를 종료하거나 특정 신호를 보낼 때 사용되는 도구
---
이 명령어는 프로세스 ID(PID)를 인수로 받아 해당 프로세스에 신호를 보낸다.

기본적으로 kill 명령어는 SIGTERM 신호(프로세스를 종료하는 신호)를 보내지만,

파이프라인(|)과 함께라면 다양한 신호도 보낼 수 있다.

(주요 옵션)
  * -l: 신호 목록을 표시합니다.
  * -s <signal>: 특정 신호를 보냅니다. 신호 이름 또는 번호를 사용할 수 있습니다.
  * -n <signal>: 특정 신호 번호를 보냅니다.
  * -p: 지정된 PID에 대한 신호를 보냅니다. 기본적으로 SIGTERM을 보냅니다.
  * -<signal>: 신호 번호를 지정하여 보냅니다.

(주요 신호 체계)
  * 1 (SIGHUP): 프로세스를 다시 읽거나 재시작합니다.
  * 9 (SIGKILL): 강제 종료 신호. 즉시 프로세스를 종료합니다.
  * 15 (SIGTERM): 기본 종료 신호. 프로세스가 종료되도록 요청합니다.
  * 19 (SIGSTOP): 프로세스를 중지시킵니다.
  * 18 (SIGCONT): 중지된 프로세스를 계속 실행합니다.
