#Docker image
FROM node

# 작업 디렉토리를 설정
WORKDIR /app

# 두개의 경로
# DOT 1 -  컨테이너의 외부
# DOT 2 -  그 파일을 저장해야하는 이미지 내부의 경로
# ./는 도커 컨테이너의 현재 작업 디렉토리를 의미
# ./ === /app
COPY . /app

RUN npm install

# RUN은 이미지 생성시 바로 실행
# CMD는 이미지를 기반으로 시작될 때 실행됨
#CMD node server.js

# CMD를 특정하지 않으면 베이스 이미지가 실행되며, 그게 없는 경우 에러가 발생
# EXPOSE는 CMD 바로 위

EXPOSE 80

CMD ["node","server.js"]
# docker build .->이미지 생성



