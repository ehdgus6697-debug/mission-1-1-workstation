# 항목 5) Dockerfile 기반 웹 서버 컨테이너
# base: python:3.11-slim (직접 작성한 Flask 앱을 컨테이너화)

FROM python:3.11-slim

WORKDIR /app

# 의존성만 먼저 복사 -> 레이어 캐싱으로 재빌드 속도 최적화
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# 앱 소스 복사
COPY . .

ENV PORT=5000
EXPOSE 5000

CMD ["python", "app.py"]
