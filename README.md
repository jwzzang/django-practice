# Django Starter

Python 3.13, Django 5.2 LTS, uv 기반의 재사용 가능한 Django 프로젝트 템플릿입니다.

## 프로젝트 구조

```text
apps/          # 직접 개발하는 Django 앱
config/        # Django 프로젝트 설정
manage.py      # Django 관리 명령어
pyproject.toml  # Python 프로젝트 및 의존성
uv.lock         # 의존성 버전 고정
```

## 시작하기

```bash
uv sync
uv run python manage.py check
uv run python manage.py migrate
uv run python manage.py runserver
```

## 새로운 앱 생성

```bash
mkdir -p apps/example
uv run python manage.py startapp example apps/example
```

`apps/example/apps.py`의 `name`을 `"apps.example"`로 수정하고 `config/settings.py`의 `CUSTOM_APPS`에 `"apps.example.apps.ExampleConfig"`를 등록합니다.

## INSTALLED_APPS 구성

- `SYSTEM_APPS`: Django 기본 앱
- `THIRD_PARTY_APPS`: 외부 라이브러리 앱
- `CUSTOM_APPS`: 직접 만든 앱

세 목록을 합쳐 `INSTALLED_APPS`를 구성합니다.
