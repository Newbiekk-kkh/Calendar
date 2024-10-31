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

*** 

ERD
----------

![image](https://github.com/user-attachments/assets/871a2dd4-9781-41b3-867d-e7ddcd88a5d9)

***
SQL
---

```
CREATE TABLE `Posts` (
	`id`	int	NOT NULL,
	`UserName`	VARCHAR(255)	NULL,
	`Password`	VARCHAR(255)	NULL,
	`Title`	VARCHAR(255)	NOT NULL,
	`Content`	VARCHAR(255)	NULL,
	`CreateDate`	VARCHAR(255)	NULL,
	`UpdateDate`	VARCHAR(255)	NULL,
	`id2`	VARCHAR(255)	NOT NULL
);

CREATE TABLE `User` (
	`id`	VARCHAR(255)	NOT NULL,
	`Name`	VARCHAR(255)	NULL,
	`Email`	VARCHAR(255)	NULL,
	`Registration date`	VARCHAR(255)	NULL,
	`UpdateDate`	VARCHAR(255)	NULL
);

ALTER TABLE `Posts` ADD CONSTRAINT `PK_POSTS` PRIMARY KEY (
	`id`
);

ALTER TABLE `User` ADD CONSTRAINT `PK_USER` PRIMARY KEY (
	`id`
);
```
