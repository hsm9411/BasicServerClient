# Python 3.10 기반의 슬림한 이미지 사용
FROM python:3.10-slim

# 필수 유틸리티 설치 (vi 등 필요 시)
RUN apt-get update && apt-get install -y curl vim && apt-get clean

# 작업 디렉토리 설정
WORKDIR /app

# requirements.txt 복사 및 설치
COPY requirements.txt .

RUN pip install --no-cache-dir -r requirements.txt

# main.py 복사 (여기까지 하면 main.py 내부 코드 포함됨)
COPY main.py .

# 컨테이너 실행 시 fastapi run main.py 명령 실행
CMD ["fastapi", "run", "main.py", "--host", "0.0.0.0", "--port", "8000"]
