# :dog: 지구멍(지구의 멍멍이들)

<p align="center">
<img width="240" alt="스크린샷 2022-08-06 오전 12 48 08" src="https://user-images.githubusercontent.com/70987007/183113888-5e797b6c-c073-4778-94d0-53116533a57d.png">

</p>

<p align="center">
<strong> 지구에 사는 멍멍이들 🐶🐾! <br> 강아지 견종 분류 및 정보 제공 서비스입니다.<br> </strong>
</p>
<br>

## 💡Tech Stack

<p align="center">
<img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=TypeScript&logoColor=white"> <img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black">
<img src="https://img.shields.io/badge/Chart.js-FF6384?style=for-the-badge&logo=Chart.js&logoColor=white">

</p>  
<p align="center">
<img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=Flask&logoColor=white">  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=PyTorch&logoColor=white"> <img src="https://img.shields.io/badge/Celery-37814A?style=for-the-badge&logo=Celery&logoColor=white"> <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=for-the-badge&logo=RabbitMQ&logoColor=white"> <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=MySQL&logoColor=white"> <img src="https://img.shields.io/badge/NGINX-009639?style=for-the-badge&logo=NGINX&logoColor=white"> <img src="https://img.shields.io/badge/Gunicorn-499848?style=for-the-badge&logo=Gunicorn&logoColor=white">
  </p>
<p align="center">
<img src="https://img.shields.io/badge/Amazon AWS-232F3E?style=for-the-badge&logo=Amazon AWS&logoColor=white"> <img src="https://img.shields.io/badge/Amazon S3-569A31?style=for-the-badge&logo=Amazon S3&logoColor=white"> <img src="https://img.shields.io/badge/GitKraken-179287?style=for-the-badge&logo=GitKraken&logoColor=white"> <img src="https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=Docker&logoColor=white"> <img src="https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=Selenium&logoColor=white"> <img src="https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=Swagger&logoColor=white">
</p>

```
- Frontend : React, Chart.js
- Backend : Flask
- Web Server: Nginx
- Middleware : Gunicorn
- AI model : Pytorch
- DevOps : Docker
- Database: MySQL
- Crawling : Selenium
- API Test : Postman
- API Documentation : Swagger
- Deployment : AWS
- VCS: Git
```

## 💻 System Architecture

![image](https://user-images.githubusercontent.com/70987007/183114388-a0f03352-9191-432f-9dce-593a737c3e43.png)

## 📗 API

![image](https://user-images.githubusercontent.com/70987007/183114204-c5d0f50f-79e8-420a-aa42-4d0c34d14b36.png)

## 🚀 How to Start

### 1. Clone Repository

```
https://github.com/2022-Summer-Bootcamp-teamG/puppy-classification.git
```

### 2. Install Pacakages

```
$ cd pupppy-classification-frontend
$ yarn run build
```

### 3. Set .env file

```bash
### settings/.env
# === Database ===
RDS_HOST =
RDS_DATABASE =
RDS_USER =
RDS_PASSWORD =

# === S3Bucket ===
S3_ID =
S3_SECRET_KEY =
S3_BUCKET_REGION =
S3_BUCKET_NAME =

```

### 4. Run Docker

```
$ docker-compose up --build         # build images and run containers
$ docker-compose down               # stop running containers
$ docker-compose down -v            # stop running containers and delete its volume
```

## 📂 Directory Structure

```bash
├── README.md
├── docker-compose.prod.yml
├── docker-compose.yml
├── nginx
│   ├── Dockerfile
│   └── nginx.conf
├── puppy-classification-backend
│   ├── Dockerfile
│   ├── README.md
│   ├── app.py
│   ├── config
│   │   ├── __init__.py
│   │   ├── connection.py
│   │   ├── rdsConfig.py
│   │   └── s3Config.py
│   ├── imagenet_class_index.json
│   ├── predict.py
│   ├── requirements.txt
│   ├── tasks.py
│   ├── views.py
│   ├── weights.pt
│   └── wsgi.py
├── puppy-classification-frontend
│   ├── Dockerfile
│   ├── Dockerfile.prod
│   ├── README.md
│   ├── build
│   ├── package-lock.json
│   ├── package.json
│   ├── public
│   ├── src
│   │   ├── App.css
│   │   ├── App.tsx
│   │   ├── assets
│   │   │   ├── fonts
│   │   │   └── images
│   │   ├── components
│   │   │   ├── common
│   │   │   │   ├── Button.ts
│   │   │   │   ├── Common.ts
│   │   │   │   ├── CustomAxios.ts
│   │   │   │   ├── Header.tsx
│   │   │   │   ├── Loading.tsx
│   │   │   │   ├── Logo.ts
│   │   │   │   ├── MediaQuery.ts
│   │   │   │   ├── NotFound.tsx
│   │   │   │   ├── SearchBar.tsx
│   │   │   │   ├── SearchBarStyle.ts
│   │   │   │   └── Title.ts
│   │   │   ├── detail
│   │   │   │   ├── ChartBox.tsx
│   │   │   │   ├── DetailImage.ts
│   │   │   │   ├── FeatureBox.tsx
│   │   │   │   └── ItemBox.ts
│   │   │   ├── list
│   │   │   │   ├── CardItem.tsx
│   │   │   │   ├── CardList.tsx
│   │   │   │   ├── Categories.tsx
│   │   │   │   ├── ItemImage.ts
│   │   │   │   ├── Pagination.tsx
│   │   │   │   └── pagination.module.scss
│   │   │   ├── main
│   │   │   │   ├── Dropzone.ts
│   │   │   │   ├── ImageUploader.tsx
│   │   │   │   ├── LabelButton.ts
│   │   │   │   ├── MainImage.ts
│   │   │   │   └── PuppyButton.tsx
│   │   │   ├── result
│   │   │   │   ├── Carousel.tsx
│   │   │   │   ├── CarouselBox.tsx
│   │   │   │   └── ResultImage.ts
│   │   │   └── search
│   │   │       └── SearchCardList.tsx
│   │   ├── custom.d.ts
│   │   ├── global.d.ts
│   │   ├── index.css
│   │   ├── index.tsx
│   │   ├── logo.svg
│   │   ├── pages
│   │   │   ├── DetailPage.tsx
│   │   │   ├── ListPage.tsx
│   │   │   ├── MainPage.tsx
│   │   │   ├── ResultPage.tsx
│   │   │   └── SearchPage.tsx
│   │   ├── setupTests.ts
│   ├── tsconfig.json
│   ├── yarn-error.log
│   └── yarn.lock
├── settings
    └── .env
```

## 👨‍👩‍👧‍👧 팀원

| [최지미](https://github.com/rabbit-22) | [김혜린](https://github.com/Kim-Hye-Lin) | [박희경](https://github.com/qkrgmlrud00) | [장현우](https://github.com/aswooo) | [하도균](https://github.com/DoKyunHa) |
| :------------------------------------: | :--------------------------------------: | :--------------------------------------: | :---------------------------------: | :-----------------------------------: |
|                  사진                  |                   사진                   |                   사진                   |                사진                 |                 사진                  |
|      Leader, Front-end Developer       |       Front-end Developer, DevOps        |            Back-end Developer            |        AI, Backend-Developer        |          Front-end Developer          |
