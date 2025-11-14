# Teachable Machine Pose Model Template

Teachable Machine에서 학습한 Pose 모델을 웹에서 테스트할 수 있는 템플릿입니다.

## 📋 개요

이 프로젝트는 학생들이 [Teachable Machine](https://teachablemachine.withgoogle.com/)에서 포즈 인식 모델을 학습한 후, 해당 모델을 GitHub에 업로드하고 GitHub Pages를 통해 실시간으로 테스트할 수 있도록 만들어진 템플릿입니다.

### 현재 포함된 예시 모델

이 저장소에는 **얼굴 방향 인식 모델**이 포함되어 있습니다:
- **왼쪽**: 얼굴이 왼쪽을 바라볼 때
- **오른쪽**: 얼굴이 오른쪽을 바라볼 때
- **정면**: 얼굴이 정면을 바라볼 때
- **위**: 얼굴이 위를 바라볼 때
- **아래**: 얼굴이 아래를 바라볼 때

이 모델은 데모용이며, 자신만의 포즈 인식 모델로 교체하여 사용할 수 있습니다.

## 🚀 사용 방법

### 1. Teachable Machine에서 모델 학습 및 다운로드

1. [Teachable Machine](https://teachablemachine.withgoogle.com/)에 접속
2. "Pose Project" 선택
3. 원하는 포즈들을 학습
4. "Export Model" → "Download" 선택하여 모델 파일 다운로드

### 2. 모델 파일 추가

다운로드한 모델 파일을 `my_model/` 폴더에 넣어주세요:
- `my_model/model.json`
- `my_model/weights.bin`
- `my_model/metadata.json`

### 3. 로컬에서 테스트

브라우저 보안 정책으로 인해 로컬 웹 서버가 필요합니다.

**Python 사용 (Python 3):**
```bash
python3 -m http.server 8000
```

**Node.js 사용:**
```bash
npx http-server -p 8000
```

**VS Code 사용:**
- Live Server 확장 프로그램 설치
- index.html 우클릭 → "Open with Live Server"

브라우저에서 `http://localhost:8000` 접속

### 4. GitHub Pages로 배포

1. 이 저장소를 자신의 GitHub 계정으로 Fork 또는 복사
2. 모델 파일을 `my_model/` 폴더에 추가
3. GitHub 저장소 설정에서 Pages 활성화:
   - Settings → Pages
   - Source: Deploy from a branch
   - Branch: main / (root) 선택
   - Save
4. 몇 분 후 `https://<username>.github.io/<repository-name>/`에서 접속 가능

## ✨ 주요 기능

- ✅ 실시간 웹캠 포즈 인식
- ✅ 포즈 스켈레톤 및 키포인트 시각화
- ✅ 예측 결과 확률 표시
- ✅ 최고 확률 클래스 강조 표시
- ✅ Start/Stop 버튼으로 웹캠 제어

## 🛠 기술 스택

- TensorFlow.js 1.3.1
- Teachable Machine Pose Library 0.8
- Vanilla JavaScript
- HTML5 Canvas

## 📁 프로젝트 구조

```
tm-pose-template/
├── index.html          # 메인 웹 페이지
├── my_model/           # Teachable Machine 모델 파일 위치
│   ├── model.json
│   ├── weights.bin
│   └── metadata.json
└── README.md
```

## 🎓 교육 활용

이 템플릿은 다음과 같은 교육 목적으로 활용할 수 있습니다:

- 머신러닝/AI 기초 학습
- 포즈 인식 기술 이해
- 웹 개발 실습
- GitHub 및 버전 관리 학습
- GitHub Pages를 통한 배포 경험

## 👨‍💻 만든 사람

**Sangbong Lee**
- Email: idealbong@gmail.com

## 📝 라이선스

이 프로젝트는 교육 목적으로 자유롭게 사용 가능합니다.
