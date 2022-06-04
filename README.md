**tos란?**

top는 유닉스 계열 시스템에서 프로세스 목록을 CPU 사용률이 높은 것부터 보여주는 소프트웨어이다.
top명령어는 시스템의 프로세스와 메모리 사용상태를 5초의 간격으로 업데이트하여 화면에 출력한다.
어떤 프로세스가 CPU를 많이 차지하고 있는지 체크할때 실시간으로 보이기 떄문에 유용하다.
윈도우의 작업관리자와 같은 역할!!


***사용방법***
|옵션|설명|
|:---|---|
|-b|배치모드로 정보를 출력합니다. 실시간 상화 대화형모드로 정보를 화면에 일렬로 출력합니다.|
|-d delay|지정한 시간(delay 초)의 간격으로 정보를 업데이트하여 출력합니다.|
|-i idle|토글값이 off일때, idle 프로세스나 좀비 프로세스 정보를 출력하지 않습니다.|
|-n num|지정한 시간(num)만큼 업데이트 정보를 출력합니다.|
|-p pid|지정한 프로세스 ID(pid)의 정보만을 출력합니다.|
|-q|시간의 간격 없이 계속하여 업데이트 정보를 출력합니다.|
|-s|몇 개의 대화식 명령을 비활성화 합니다.|
|-S|누적된 정보를 출력합니다.|

top명령어를 실행한 후 초기화면에서 "h"키를 입력하면 사용할수있는 단축키 목록을 확인할수 있다.
***전체내용***

<img width="402" alt="image" src="https://user-images.githubusercontent.com/106620115/171995545-a203e23d-8bbb-4a87-981b-5b9360f172e1.png">

***첫번째 줄***
<img width="405" alt="image" src="https://user-images.githubusercontent.com/106620115/171995608-436d1c4c-b966-4139-b0e6-34981c0d86f8.png">
**서버 정보를 담고 있는 줄**
top - 12:25:57 >>>> 12시 25분 57초 현재 서버의 시간
up >>> 가동 중
2:30 >>>> 2시간 30분째
2 users >>>> 2명의 사용자가 접속
load average:0.00, 0.00, 0.00 >>> load average(부화율)
***두번째 줄***
<img width="407" alt="image" src="https://user-images.githubusercontent.com/106620115/171995752-2aab4901-731a-468d-bbdb-de13e06ad0d6.png">
**프로세스 정보를 담고 있는 줄**
105 total >>> 총 105개의 프로세스 가동 중
1 running >>> 1개의 프로세스가 실행 중
102 sleeping >>> 102개의 프로세스가 대기 중
2 stoppend >>> 2개의 프로세스가 멈춤
0 zombie >>> 0개의 프로세스 좀비 상태
***세번째 줄***
<img width="401" alt="image" src="https://user-images.githubusercontent.com/106620115/171995870-d65d864c-e8b7-4f6a-be54-30d42a3c5bff.png">
**CPU 정보를 담고 있는 줄**
% us >>> 유저레벨에서 사용하고 있는 CPU 비중
% sy >>> 시스템 레벨에서 사용하고 이쓴 CPU 비중
% id >>> 유휴 상태의 CPU 비중
% wa >>> 시스템이 I/O 요청을 처리하지 못한 상태에서의 CPU idle 상태인 비중
***네번쨰와 다섯번째 줄***
<img width="406" alt="image" src="https://user-images.githubusercontent.com/106620115/171995982-95c8d617-abc1-4669-9055-9ac58d852ca4.png">
**메모리 정보를 담고 있는 줄**
MiB Mem
1827.1 total >>> 전체 물리적인 메모리
1276.4 free >>> 사용되지 않는 여유 메모리
250.5 used >>> 사용중인 메모리
300.2 buff/cache >>> 버퍼된 메모리
Swap
5120.0 total >>> 전체 스왑 메모리
5120.0 free >>> 사용되지 않은 여유 메모리
0.0 used >>> 사용 중인 스왑 메모리
1426.0 avail Mem >>> 캐싱메모리
***그 이 하 내용***
**프로세스 상태**
<img width="407" alt="image" src="https://user-images.githubusercontent.com/106620115/171996307-864fbd84-dfec-4f71-951e-ee70c1847a04.png">
|PID|프로세스 ID(PID)|
|USER|프로세스를 실행시킨 사용자ID|
|PR|프로세스의 우선순위(priority)|
|NI|NICE 값.알의 nice value 값.마이너스를 가지는 nice value는 우선순위가 높음|
|VIRT|가상 메모리의 사용량(SWAP+RES)|
|RES|현재 페이지가 상주하고 있는 크기(Resident Size)|
|SHR|분할된 페이지,프로세스에 의해 사용된 메모리를 나눈 메모리의 총 합|
|S|프로세스의 상태-S(sleeping),R(running),W(swqpped out process),Z(zombies)|
|%CPU|프로세스가 사용하는 CPU의 사용률|
|%MEM|프로세스가 사용하는 메모리의 사용률|
|COMMAND|실행된 명령어|


