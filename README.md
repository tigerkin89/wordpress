# wordpress for Ubuntu
우분트 14.04에 WordPress를 설치합니다.

## docker 이미지 생성
```ruby
$ sudo docker build --tag wordpress .
```
## container 실행
wordpress container 실행하기 전에 DB container ( https://github.com/tigerkin89/mysql ) 를 먼저
실행하여 주식 바랍니다.

```ruby
docker run -d --name example-wp -p 80:80 --link db:db wordpress
```

## Git upload
```ruby
$git init 
$git add *
$git commit -m "ffff" 
$git branch -M main git remote add origin https://github.com/tigerkin89/wordpress 
$git push origin +main
```
## 해설
Dockerfile, entrypoint.sh에 대한 자세한 설명은 여기
( http://pyrasis.com/book/DockerForTheReallyImpatient/Chapter16/ )를
참고바립니다.
