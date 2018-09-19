# docker-eb-deploy 구현

### 초기 설정
    take (deploy사용할폴더만들기) -> git init -> .gitignore -> pipenv install django 
    -> django-admin startproject (config사용할 프로젝트이름) -> mv config app(config를 app으로 변경)
    -> app root설정 -> 파이참 interpreter설정
    
### .secrets/base.json 설정
+ settings 파일 패키지화 해주기
    
    
    settings 파일 패키지화 해주고 안에 base.py, local.py 파일을 추가 시켜준다.
    __init__.py 안에 있는 설정파일을 base.py에 옮겨준다. 
    설정파일을 base.py, local.py에 분류
    
    
> base.py -> base.json으로부터 SECRET_KEY할당(언어변경, 한국시간으로 변경, 경로 설정(templates, static, media, secrets 등등))

> local.py -> DEBUG, ALLOWED_HOSTS, WSGI_APPLICATION, DATABASES, STATIC_URL 를 base.py 안에서 코드 잘라오기