# upgraded 폴더 구조 설명

`upgraded` 폴더는 레거시(`legacy`) 폴더의 전체 파일과 디렉터리 구조를 복사한 것으로, Python 프로젝트의 업그레이드 실습을 위한 작업 공간입니다.

## 최상위 파일 및 폴더
- `MANIFEST.in` : 패키징 시 포함할 파일 목록을 지정하는 설정 파일
- `README.rst` : 프로젝트 설명 문서 (reStructuredText 형식)
- `distribute-0.6.10.tar.gz`, `distribute_setup.py` : 레거시 Python 패키징 도구 관련 파일
- `setup.py` : 프로젝트 설치 및 배포를 위한 파이썬 스크립트
- `docs/` : 프로젝트 문서화 관련 디렉터리
- `guachi/` : 주요 Python 패키지 소스 코드 및 테스트 코드가 위치
- `guachi.egg-info/` : 패키지 메타데이터 정보 디렉터리

## docs/
- `Makefile` : 문서 빌드 자동화용 Makefile
- `build/` : 빌드된 문서 결과물 저장 디렉터리
  - `doctrees/` : Sphinx 문서 빌드 중간 산출물
  - `html/` : HTML로 변환된 문서와 정적 파일
- `source/` : Sphinx 문서 소스
  - `.rst` 파일들(각종 설명, 가이드)
  - `_static/` : 커스텀 CSS 등 정적 리소스

## guachi/
- `__init__.py`, `config.py`, `database.py` : 주요 모듈 파일
- `tests/` : 단위 테스트 코드
  - `test_configmapper.py`, `test_configurations.py`, `test_database.py`, `test_integration.py`

## guachi.egg-info/
- 패키지 배포를 위한 메타데이터 파일들

이 구조는 레거시 Python 프로젝트의 전형적인 구성으로, 업그레이드 실습 및 테스트에 활용됩니다.
