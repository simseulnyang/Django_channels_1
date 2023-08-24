# Django_channels_1
- Django Channels를 활용한 비동기 웹 애플리케이션 연습
<br>
## Overview
![gif](/README/전체%20v1.gif)
<br>
## 개발환경

    - Django 4.2.4 (Python 3.11.3)
    - Django-channels 3.0.4
    - HTML5
    - Tailwind
    - sqlite3

<br>
## 설치 및 실행
- 현재 github repository를 clone하여 로컬에 폴더를 생성합니다.
- 사용하는 IDE를 열고 가상환경을 생성합니다.
```
    # 1. 가상환경 생성
    
    # 가상환경설정이름에 설정하고자 하는 가상환경이름을 넣습니다.
    
        python -m venv 가상환경설정이름


    # 2. 가상환경 활성화 => 커맨드 라인 앞에 (venv)가 생성됩니다.
    # macOS
        source venv/bin/activate
    # PowerShell
        venv/Scripts/Activate.ps1
    # CMD
        call venv/Scripts/activate.bat
    # Git Bash
        source venv/Scripts/activate
```
- 의존성 설치를 시작합니다. (가상환경이 활성화 된 상태에서 실행)
```
    pip install -r requirements.txt
```
- 데이터 마이그래이션을 진행합니다.
```
    python manage.py migrate
```
- 개발 서버를 실행합니다.
```
    python manage.py runserver

    실행주소
    http://127.0.0.1:8000/
```

<br>
## 프로젝트 구조
```
django-channels_1
├── core
│   ├── templates
│   │    └── core
│   │         ├── base.html      
│   │         ├── frontpage.html      
│   │         ├── login.html       
│   │         └── signup.html      
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── mysite
│   ├── __init__.py
│   ├── asgi.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── room
│   ├── templates
│   │    └── room
│   │         ├── room.html          
│   │         └── rooms.html      
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── consumers.py
│   ├── models.py
│   ├── routing.py
│   ├── tests.py
│   ├── urls.py
│   └── views.py
├── README
├── manage.py
├── README.md
└── requirements.txt
```

<br>
## 개발기간
    - 2023-08-22 ~ 2023-08-24


<br>
## 현재(v1.0.0) 문제점
1. 유저 간 소통이 아닌 유저 한명당 1소통만 진행됨