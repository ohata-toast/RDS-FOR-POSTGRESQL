## Database > RDS for PostgreSQL > 알림

## 사용자 그룹

알림을 받을 사용자를 그룹으로 관리할 수 있습니다. 알림 대상은 반드시 프로젝트 멤버로 등록되어 있어야 합니다. 사용자 그룹에 속한 사용자가 프로젝트 멤버에서 제외되면 사용자 그룹에 속해 있더라도 알림을 받을 수 없습니다.

> [주의]
> 실명 인증을 진행하지 않아 휴대폰 정보가 없을 경우 SMS 알림을 받을 수 없습니다.

### 사용자 그룹 생성

![user_group_01_ko](https://static.toastoven.net/prod_rds/23.06.13/user_group_01_ko.png)

* ❶ **사용자 그룹 생성**을 누르면 사용자 그룹을 생성할 수 있는 팝업 창이 나타납니다.
* ❷ 사용자 그룹에 추가된 사용자가 나타납니다.
* ❸ **x**를 누르면 추가된 사용자를 제외할 수 있습니다.
* ❹ 사용자 목록에 사용자가 많을 경우 검색 조건을 입력하여 결과를 제한할 수 있습니다.
* ❺ **전체 프로젝트 멤버**를 통보 대상에 추가합니다. 
  * 추가 시 개별 사용자 추가는 취소됩니다.
  * 해당 사용자 그룹을 이용하여 알람을 전송하게 되는 경우, 당시 전체 프로젝트 멤버 대상으로 알람을 전송합니다.
* ❻ **확인**를 눌러 사용자 그룹에 사용자를 추가합니다.

## 알림 그룹

알림 그룹을 통해 성능 지표에 대한 알림을 받을 수 있습니다. 알림 그룹에 감시 대상 인스턴스와 알림을 받을 사용자 그룹을 지정합니다. 감시 설정을 통해 알림을 받을 성능 지표의 임겟값과 조건을 설정합니다. 설정된 지표가 감시 설정의 조건을 충족하면 연결된 사용자 그룹에 알림을 발송하게 됩니다. 알림 그룹에 설정된 알림 유형에 따라 SMS 혹은 메일로 알림을 발송합니다.

### 알림 그룹 생성

![notification_group_01_ko.png](https://static.toastoven.net/prod_rds/23.04.11/notification_group_01_ko.png)

* ❶ **그룹 만들기**를 누르면 알림 그룹을 생성할 수 있는 팝업 창이 나타납니다.
* ❷ 알림을 받을 방법을 선택합니다.
* ❸ 활성화되지 않은 알림 그룹은 알림 발송을 하지 않습니다.
* ❹ 감시 대상 DB 인스턴스를 선택합니다.
* ❺ 알림을 받을 사용자 그룹을 선택합니다.

## 감시 설정

감시 설정은 감시 항목, 비교 방법, 임겟값 및 지속 시간으로 구성됩니다. 감시 항목의 성능 지푯값과 임겟값을 비교하여 조건이 충족하는지 판단합니다. 조건이 지속 시간 이상 연속해서 충족한다면 알림을 발송합니다. 예를 들어, CPU 사용률의 임겟값이 90% 이상이고 지속 시간이 5분이라면, 해당 알림 그룹과 연동된 DB 인스턴스의 CPU 사용률이 90% 이상인 상태가 5분 이상 지속되었을 때 사용자 그룹에 정의된 사용자들에게 알림을 보냅니다. 만약 CPU 사용률이 90% 이상이 되어도, 5분 이내에 90% 미만으로 떨어지면 알림이 발생하지 않습니다.

### 감시 설정 항목

감시 가능한 성능 지표 항목은 다음과 같습니다.

| 힝목                         | 단위                 |
|----------------------------|--------------------|
| CPU 사용률                    | %                  |
| CPU 사용량(IO Wait)           | %                  |
| CPU 사용량(Nice)              | %                  |
| CPU 사용량(System)            | %                  |
| CPU 사용량(User)              | %                  |
| Load Average 1M            |                    |
| Load Average 5M            |                    |
| Load Average 15M           |                    |
| 메모리 사용량                    | %                  |
| 메모리 사용량(바이트)               | MB                 |
| 메모리 여유량(바이트)               | MB                 |
| 메모리 버퍼(바이트)                | MB                 |
| 캐시된 메모리(바이트)               | MB                 |
| 스왑 사용량                     | MB                 |
| 스왑 전체 크기                   | MB                 |
| Storage 사용량                | %                  |
| Storage 남은 사용량             | MB                 |
| Storage IO Read            | KB/sec             |
| Storage IO Write           | KB/sec             |
| 데이터 스토리지 결함                | 비정상: 0, 정상: 1      |
| Network in BPS             | KB/sec             |
| Network out BPS            | KB/sec             |
| Database Connection Status | 접속 불가: 0, 접속 가능: 1 |
| Queries Per Second         | counts/sec         |
| Lock Tables                | counts/sec         |
| Cache Hit Ratio            | %                  |
| Idle Connection            | counts/sec         |
| Active Connection          | counts/sec         |
| Total Connection           | counts/sec         |
| Fetched Tuple Count        | counts/sec         |
| Returned Tuple Count       | counts/sec         |
| Inserted Tuple Count       | counts/sec         |
| Updated Tuple Count        | counts/sec         |
| Deleted Tuple Count        | counts/sec         |
| Transaction Commit         | counts/sec         |
| Transaction Rollback       | counts/sec         |
| Deadlock                   | counts/sec         |
| Conflict                   | counts/sec         |

### 감시 설정 추가

![notification_group_02_ko.png](https://static.toastoven.net/prod_rds/23.04.11/notification_group_02_ko.png)

* ❶ **감시 설정**을 누르면 감시 설정을 변경할 수 있는 팝업 창이 나타납니다.
* ❷ **감시 설정 추가** 를 눌러 신규 감시 설정을 추가합니다.
* ❸ 감시할 항목과 비교 방법, 임곗값, 지속 시간을 입력한 뒤 **추가**를 클릭합니다.

### 감시 설정 변경 및 삭제

![notification_group_03_ko.png](https://static.toastoven.net/prod_rds/23.04.11/notification_group_03_ko.png)

* ❶ 버튼을 클릭하면 추가된 감시 설정을 변경할 수 있습니다.
* ❷ 버튼을 클릭하면 추가된 감시 설정을 삭제할 수 있습니다.
