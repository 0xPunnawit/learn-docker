# โหลด image
FROM node:22.20.0

# กำหนด directory ที่จะเก็บไฟล์โปรเจค
WORKDIR /app

# คัดลอกไฟล์ ไปยัง directory ที่กำหนดไว้
COPY package*.json ./

# ติดตั้ง package ที่ระบุไว้ใน json
RUN npm install

# ติดตั้ง nodemon เพื่อใช้ในการรันโปรเจค
RUN npm install -g nodemon

# คัดลอกไฟล์ทั้งหมดไปยัง directory ที่กำหนดไว้ แต่ ตรวจสอบด้วยว่า .dockerignore มีอะไรบ้าง จะไม่ Copy ลงไป
# . แรกเครื่องเรา
# . ที่สอง root path app
COPY . .

EXPOSE 3000

CMD [ "npm", "run", "dev" ]