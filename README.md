# Sparta_Schedule

## API 명세서 작성
https://documenter.getpostman.com/view/39376424/2sAY4vhi4F

## ERD 작성
<img width="651" alt="스크린샷 2024-10-31 오후 8 33 18" src="https://github.com/user-attachments/assets/a3368062-cc71-4123-ac82-2f5c953b76d7">



## SQL 작성
```
//Schedule 테이블 생성
CREATE TABLE `Schedule` (
  `id` int NOT NULL,
  `user_name` varchar(20) COLLATE utf8mb3_bin NOT NULL,
  `password` int NOT NULL,
  `title` varchar(45) COLLATE utf8mb3_bin NOT NULL,
  `content` varchar(200) CHARACTER SET utf8mb3 COLLATE utf8mb3_bin DEFAULT NULL,
  `create_date` datetime DEFAULT NULL,
  `update_date` datetime DEFAULT NULL,
  `user_id` int NOT NULL,
  PRIMARY KEY (`id`)
);

//User 테이블 생성
CREATE TABLE `Sparta_Schedule`.`User` (
  `id` INT NOT NULL,
  `name` VARCHAR(45) NOT NULL,
  `password` INT NOT NULL,
  `create_date` DATETIME NULL,
  `update_date` DATETIME NULL,
  PRIMARY KEY (`id`)
);
```
