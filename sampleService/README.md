# 도커 배포명령

## 빌드
docker build -t docker.webnori.com/node-web-app .

## 테스트
docker run -p 8080:8080 -d docker.webnori.com/node-web-app

## 배포
docker push docker.webnori.com/node-web-app

