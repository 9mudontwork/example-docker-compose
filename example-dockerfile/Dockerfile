FROM postgres:latest
RUN mkdir /root/data

# กำหนด root folder และ ถ้ากำหนด root folder เวลาเข้า shell จะเข้าไปที่ folder นั้นเลย
WORKDIR /root/data

COPY src .
# COPY src /root/data

# ตัวอย่างวหากต้องการติดตั้ง vim
# -y คือให้ยอมรับอัตโนมัติ หลังจากอัปเดตเสร็จ ให้ติดตั้ง vim เข้าไปด้วย
# \ คือตัวต่อคำสั่ง ถ้าหากมันยาว
# rm -rf ลบไฟล์ repo package ที่โหลดมา
RUN apt-get update -y && \
    apt-get install -y vim && \
    rm -rf /var/lib/api/lists/*
