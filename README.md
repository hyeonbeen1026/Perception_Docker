# Perception Team Docker Environment

이 저장소는 인지(Perception) 모듈 개발을 위한 ROS 2 Humble 및 Deep Learning(PyTorch, YOLO) 환경 세팅을 포함하고 있습니다.

## 1. 도커 이미지 빌드 (최초 1회)
저장소를 클론(다운로드)한 후, 파일이 있는 폴더에서 터미널을 열고 아래 명령어를 실행하세요.
(용량이 커서 시간이 다소 소요될 수 있습니다.)

```bash
docker build -t perception_env .
