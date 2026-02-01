# Lumora Tools

블로그 **Lumora** 운영 및 일반 사용자를 위한 웹 기반 유틸리티 모음입니다.  
모든 툴은 **서버 전송 없이(Serverless)** 브라우저 내에서 안전하게 작동하며, **다크 모드(Dark Mode)** 기반의 일관된 디자인 시스템이 적용되어 있습니다.

---

## 🛠️ 제공되는 툴 (Tools)

| 툴 이름 (Tool) | 경로 (Path) | 설명 (Description) | 주요 기능 |
| :--- | :--- | :--- | :--- |
| **이미지 용량 줄이기** | [이미지 용량 줄이기](./img-compressor/index.html) | JPG, PNG, WEBP 등 이미지 파일의 용량을 줄여주는 도구입니다. | 📉 용량 압축<br>📏 사용자 지정 리사이즈<br>🔍 줌/팬 미리보기 |
| **PDF → 이미지 변환** | [`converters/pdf-image/`](./converters/pdf-image/index.html) | PDF의 각 페이지를 이미지(JPG/PNG)로 변환합니다. | 📦 ZIP 압축 다운로드<br>📱 모바일 최적화<br>🔒 보안 (로컬 처리) |
| **이미지 → PDF 변환** | [`converters/image-pdf/`](./converters/image-pdf/index.html) | 여러 장의 이미지를 하나의 PDF 파일로 병합합니다. | 📑 순서 변경 지원<br>⚡ 빠른 변환 |
| **PDF 합치기** | [`converters/pdf-merge/`](./converters/pdf-merge/index.html) | 여러 개의 PDF 파일을 하나로 합칩니다. | 📑 순서 변경(Drag)<br>⚡ 대용량 지원(로컬) |
| **HEIC → JPG 변환** | [`converters/heic → jpg/`](./converters/heic%20→%20jpg/index.html) | 아이폰 사진(HEIC)을 웹용 이미지(JPG)로 변환합니다. | 🍎 아이폰 호환<br>🖼️ 미리보기 지원 |
| **PNG ↔ JPG 변환** | [`converters/png-jpg/`](./converters/png-jpg/index.html) | PNG와 JPG 포맷을 상호 변환합니다. | 🔄 간편 변환 |
| **ICO 변환기** | [`converters/ico/`](./converters/ico/index.html) | 이미지를 파비콘(Favicon)용 ICO 파일로 변환합니다. | 🎨 파비콘 제작 |
| **해외 직구 사이즈 변환기** | [`converters/global-size-converter/`](./converters/global-size-converter/index.html) | 신발, 의류, 모자, 반지 등 해외 직구 시 필요한 사이즈를 변환해줍니다. | 👟 신발, 👕 의류, 🧢 모자, 💍 반지<br>⚡ 실시간 변환 |

---

## 🎨 디자인 시스템 (Design System)

Lumora Tools는 일관된 사용자 경험을 위해 자체 디자인 시스템을 따릅니다.
새로운 툴을 개발하거나 기여하실 때는 아래 가이드를 참고해 주세요.

-   **Color Palette**: 
    -   배경: `#1e1e1e` (Dark Gray)
    -   포인트: `#a78bfa` (Light Purple)
-   **Typography**: `'Noto Sans', system-ui, sans-serif`
-   **Features**:
    -   모든 컴포넌트는 `#id`로 스타일이 격리(Scoped)되어야 합니다.
    -   모바일 반응형 레이아웃을 기본으로 지원해야 합니다.

---

## 🚀 사용 방법 (How to use)

1.  이 저장소를 클론하거나 다운로드합니다.
2.  원하는 툴의 폴더로 이동하여 `index.html` 파일을 크롬(Chrome) 등 최신 브라우저에서 엽니다.
3.  별도의 설치나 서버 구동 없이 즉시 사용 가능합니다.

---

## 📌 향후 계획 (Roadmap)
- [ ] 공통 CSS/JS 모듈화 (중복 코드 제거)
- [ ] GitHub Pages 배포 자동화
- [ ] WebP 변환기 전용 툴 추가

---

## 📄 License
이 저장소의 코드는 [MIT License](LICENSE) 하에 공개됩니다.
