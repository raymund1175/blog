1) 기본 문법
```python
docker cp [컨테이너_ID]:[컨테이너_내부_경로] [호스트_저장_경로]
```
2) 컨테이너 루트(`/`)부터 다 가져오고 싶을 때
```python
docker cp [컨테이너 ID]:/ [호스트_저장_경로]
```
3) 특정 폴더의 '내용물만' 다 가져오고 싶을 때: 폴더 경로 끝에 `.`(점) 붙이기
```python
docker cp [컨테이너 ID]:{folder_path}/. [호스트_저장_경로]

# 예시: 컨테이너 안의 /app/code 폴더를 현재 디렉토리로 가져오기 docker cp 1a2b3c4d5e6f:/app/code ./my_downloaded_code
```
