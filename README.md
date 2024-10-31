# 일정관리 앱

API 명세서
--------------

| 기능 | Method | **URL** | **request** | **response** | **상태코드** |
| --- | --- | --- | --- | --- | --- |
| 일정 등록 | POST | /api/schedules  |  |  | 200 OK |
| 전체 일정 조회 | GET | /api/schedules |  |  | 200 OK |
| 선택 일정 조회 | GET | /api/schedules/{schedules_id} |  |  | 200 OK |
| 일정 수정 | PUT | /api/schedules/{schedules_id}  |  |  | 200 OK |
| 일정 삭제 | DELETE | /api/schedules/{schedules_id}  |  |  | 200 OK |

ERD
----------

![image](https://github.com/user-attachments/assets/871a2dd4-9781-41b3-867d-e7ddcd88a5d9)
