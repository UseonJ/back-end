- MySQL 한 번에 끝내기
- MySQL 소개
- MySQL 

1. 다운로드

오라클 계정 필요. > 프리티어 가입 오류가 많다고 함. 가입실패...

![sql의 분류](image-12.png)

실행 = ctrl enter


SHOW DATABASE

USE db_name

SHOW TABLES (STATUS)

DESC(RIBE) table_name

SELECT * FROM table_name
'*' : all을 의미

SELECT field_name 
FROM table_name
WHERE 조건식

여기에 관계연산자 사용가능
OR, AND, NOT, 조건연산자 등
BETWEEN ... AND ... 도 사용가능

IN()
LIKE() - %,_

Sub Query
SELECT * FROM table_name
WHERE CountryCode = (SELECT CountryCode FROM city WHERE Name = Seoul))

SELECT * FROM table_name
WHERE Population > ANY = (SELECT Population FROM city WHERE Name = 'Seoul'))

ORDER BY Population (DESC)

정렬, 오름차순이 기본.

DISTINCT

LIMIT 10

GROUP BY CountryCode
집계함수를 함께사용
![집계함수란](image-13.png)

SELECT CountryCode, AVG(Population) AS 'Average' FROM city GROUP BY CountryCode