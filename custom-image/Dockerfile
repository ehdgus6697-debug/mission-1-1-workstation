# 항목 7) 기존 Dockerfile 기반 커스텀 이미지 제작
# 선택: (A) 웹 서버 베이스 이미지 활용 + 정적 콘텐츠 교체
# 기존 베이스: nginx:alpine (공식 이미지)

FROM nginx:alpine

LABEL org.opencontainers.image.title="my-custom-nginx"
LABEL org.opencontainers.image.description="Codyssey mission 1-1 custom nginx image"

# 커스텀 포인트 1: 환경변수로 환경 구분 표시
ENV APP_ENV=dev

# 커스텀 포인트 2: 기본 nginx welcome 페이지를 내가 만든 정적 페이지로 교체
COPY site/ /usr/share/nginx/html/
RUN chmod -R a+rX /usr/share/nginx/html

EXPOSE 80
