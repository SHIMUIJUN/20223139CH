 **리눅스 명령어 조사 과제**
------
## 1. top
------
>-시스템의 프로세스/메모리 사용 상태를 5초 간격으로 업데이트하여 출력

>-기본 출력
>>현재 시간, 시스템 업데이트 시간, 시스템에 로그인한 사용자 수, 지난 1분, 5분 15분간의 시스템 평균 부하, 프로세스 정보, CPU 상태, 메모리와 스왑 생태

>옵션
>|옵션|효과|
>|---|---|
>|-b|배치모드로 정보를 출력, 실기낙 상화 대화형모드로 정보를 화면에 일렬로 출력|
>|-d delay|지정한 시간의 간격으로 정보를 업데이트하여 출력|
>|-i idel|토글값이 off일 때, idle 프로세스나 좀비 프로세스 정보를 출력하지 안함|
>|-n num|지정한 시간만큼 업데이트 정보를 출력|
>|-p pid|지정한 프로세스 ID의 정보만을 출력|
>|-q|시간의 간격 없이 계속하여 업데이트 정보를 출력|
>|-s|몇 개의 대화식 명령을 비활성|
>|-S|누적된 정보를 출력|

>단축키
>|명령어|설명|
>|---|---|
>|space|정보를 업데이트|
>|^L|스크린 초기화|
>|F or f|필드 추가 or 제거|
>|O or o|출력하는 필드의 정렬 순서를 변경|
>|h or ?|사용 가능한 명령어를 출력|
>|k|프로세스를 종료|
>|n or #|출력할 프로세스 수를 지정|
>|s|출력할 정보의 업데이트 시가 지정|
>|W|~/.toprc에 설정된 내용을 저장|
>|q|top을 종료|
>|S|cumulative 모드를 선택 or 해제|
>|i|idle 프로세스 정보를 출력 or 해제|
>|I|Irix나 솔라리스 정보를 출력 or 해제|
>|c|명령행에서 실행한 명령어 자체로 출력 or 해제|
>|l|로드 평균 정보를 출력 or 해제|
>|m|메모리 정보를 출력 or 해제|
>|t|요약된 정보만을 출력 or 해제|
>|r|프로세스 우선순위 변경|
>|N|pid 정보를 기준으로 정렬|
>|A|age 정보를 기준으로 정렬|
>|P|CPU 사용량을 기준으로 정렬|
>|M|적재된 메모리 사용량을 기준으로 정렬|
>|T|시간/누적시간을 기준으로 정렬|
>|u|지정한 사용자의 정보만을 출력|

------
## 2. ps
------
>-프로세스의 현재 상태를 출력

>-기본 출력
>>PID, TTY, TIME, CMD

>|옵션|설명|
>|---|---|
>|-A|모든 프로세스 출력|
>|-N|ps 프로세스 제외 출력|
>|-a|세션 리더 및 터미널에 속하지 않는 프로세스 제외 출력|
>|-d|세션 리더를 제외한 모든 프로세스 출력|
>|-e|커널 프로세스를 제외한 모든 프로세스를 출력|
>|T|현재 터미널에서의 모든 프로세스를 출력|
>|a|현재 터미널은 사용자 고유 프로세스 출력|
>|r|현재 실행 중인 프로세스 출력|
>|x|터미널이 없는 프로세스를 출력|
>|--deselect|-N옵션과 같음|
>|-C|지정한 명령어의 이름에 관련된 정보를 출력|
>|-G|그룹 ID에 관련된 정보를 출력|
>|-U|사용자 ID에 관련된 정보를 출력|
>|-g|지정한 세션 리더 혹은 그룹명에 관련한 정보를 출력|
>|-p|프로세스 ID를 출력|
>|-s|세션에 속한 프로세스를 지정|
>|-t|tty를 지정|
>|-u|사용자 ID를 지정|
>|U|지정한 사용자의 프로세스를 출력|
>|p|프로세스 ID를 지정|
>|t|tty를 지정|
>|--Group|실제 그룹 이름이나 ID를 지정|
>|--User|실제 사용자 이름이나 ID를 지정|
>|--group|유효 사용자 이름이나 ID를 지정|
>|--pid|프로세스 ID를 지정|
>|--sid|세션 ID를 지정|
>|--tty|터미널을 지정|
>|--user|유효 사용자 이름이나 ID를 지정|
>|-123|--sid 123과 같은 의미|
>|123|--pid 123과 같은 의미|

------
## 3. jobs
------
>-작업이 중지된 상태, 백그라운드로 진행 중인 작업 상태, 변경되었지만 보고되지 않은 상태 표시

>-기본 출력
>>Running, Done, Done(code), Stopped, Stopped(SIGTSTP), Stopped(SIGSTOP), Stopped(SIGTTIN), Stopped(SIGTTOU)

>옵션
>|옵션|설명|
>|---|---|
>|-l|프로세스 그룹 ID를 state 필드 앞에 출력|
>|-n|프로세스 그룹 중에 대표 프로세스 ID를 출력|
>|-p|각 프로세스 ID에 대해 한 행씩 출력|
>|command|지정한 명령어를 실행|

------
## 4. kill
------
>-프로세스 종료

>옵션
>|옵션|설명|
>|---|---|
>pid ···|종료시킬 프로세스 ID나 프로세스 이름을 지정|
>|-s|전달할 시그널의 종류를 지정|
>|-l|시그널로 사용할 수 있는 시그널 이름들을 보여줌|
>|-1,|-HUP 프로세스를 재활성화|
>|-9|프로세스를 강제로 종료|

------

Vim 에디터 매크로 사용법
>순서
>1. q(매크로 시작)
>2.(매크로명 지정을 위한 아무 키 입력)
>3. 매크로 내용 입력
>4. q(매크로 종교)
>5. @매크로명 (매크로명인 매크로를 실행)

>N@매크로명 = 매크로명인 매크로를 N만큼 실행
>@@ = 방금 실행한 매크로 실행
