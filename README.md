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
  `user_name` varchar(20) NOT NULL,
  `password` int NOT NULL,
  `title` varchar(45) NOT NULL,
  `content` varchar(200),
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

ALTER TABLE `Sparta_Schedule`.`Schedule` 
ADD INDEX `user_id_idx` (`user_id` ASC) VISIBLE;
;
ALTER TABLE `Sparta_Schedule`.`Schedule` 
ADD CONSTRAINT `user_id`
  FOREIGN KEY (`user_id`)
  REFERENCES `Sparta_Schedule`.`User` (`id`)
  ON DELETE NO ACTION
  ON UPDATE NO ACTION;
```
