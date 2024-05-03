FROM python:3.9-alpine

# 更新系統套件
RUN apk update

# 設定工作目錄
WORKDIR /app

# 複製並安裝相依套件
COPY requirements.txt requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

# 複製整個程式碼到容器中
COPY . .

# 設定 Python 環境變數
ENV PYTHONUNBUFFERED=1

# 定義執行指令
CMD ["flask", "run", "--host=0.0.0.0", "--port=5000"]
