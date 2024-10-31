# 일정관리 앱

API 명세서
--------------

| 기능 | Method | **URL** | **request** | **response** | **상태코드** |
| --- | --- | --- | --- | --- | --- |
| 일정 등록 | POST | /api/schedules  | 요청 body <br> {<br>'UserName'<br>'Password'<br>'Title'<br>'Content'<br>} | 등록 정보 | 200 OK, 400 비정상 값 |
| 전체 일정 조회 | GET | /api/schedules |  | 다건 응답 정보 | 200 OK |
| 선택 일정 조회 | GET | /api/schedules/{schedules_id} | 요청 param(id) | 단건 응답 정보 | 200 OK |
| 일정 수정 | PUT | /api/schedules/{schedules_id}  | 요청 param(id), 요청 body | 수정 정보 | 200 OK, 400 비정상 값 |
| 일정 삭제 | DELETE | /api/schedules/{schedules_id}  | 요청 param(id) | 삭제 정보 | 200 OK, 404 선택한 일정이 사라짐 |

*** 

ERD
----------

![image](https://github.com/user-attachments/assets/09617f27-30d9-4422-aaec-409db770ba62)



***
SQL
---

```
CREATE TABLE `Posts` (
	`id`	int	NOT NULL,
	`UserName`	VARCHAR	NOT NULL,
	`Password`	VARCHAR	NOT NULL,
	`Title`	VARCHAR	NOT NULL,
	`Content`	VARCHAR	NULL,
	`CreateDate`	TIMESTAMP	NULL,
	`UpdateDate`	TIMESTAMP	NULL,
	`id2`	VARCHAR(255)	NOT NULL
);

CREATE TABLE `User` (
	`id`	int	NOT NULL,
	`Name`	VARCHAR	NOT NULL,
	`Email`	VARCHAR	NOT NULL,
	`Registration date`	TIMESTAMP	NULL,
	`UpdateDate`	TIMESTAMP	NULL
);

ALTER TABLE `Posts` ADD CONSTRAINT `PK_POSTS` PRIMARY KEY (
	`id`
);

ALTER TABLE `User` ADD CONSTRAINT `PK_USER` PRIMARY KEY (
	`id`
);
```
