# Lumora Tools

블로그 **Lumora** 운영에 필요한 각종 변환기 및 유틸리티를 모아둔 저장소입니다.  
(PNG/JPG 변환기, PDF 변환기, ICO 변환기 등)

---

## 📂 구조

lumora-tools/

├─ converters/ # 변환기 모음

│ ├─ png-jpg/ # PNG ↔ JPG 변환기

│ ├─ pdf-image/ # PDF ↔ 이미지 변환기

│ └─ ico/ # PNG/JPG → ICO 변환기

├─ common/ # 공통 코드/스타일

└─ docs/ # 사용 가이드

yaml
코드 복사

---

## 🛠️ 현재 제공되는 툴
- **PNG ↔ JPG 변환기**  
  간단히 이미지 포맷을 서로 변환  

- **PDF ↔ 이미지 변환기**  
  여러 장의 PDF를 이미지로, 이미지들을 PDF로 합치기  

- **PNG/JPG → ICO 변환기**  
  아이콘 제작용 변환기  

---

## 🚀 사용 방법
1. 원하는 변환기 폴더로 이동  
2. `index.html` 파일을 열면 브라우저에서 바로 실행 가능  
3. 블로그에는 `script.js`와 `style.css`를 불러와서 삽입 가능  

---

## 📌 향후 계획
- 공통 UI 컴포넌트 정리 (`common/` 활용)
- GitHub Pages를 통한 온라인 데모 제공
- 변환 속도 최적화 및 모바일 대응 개선

---

## 📄 License
이 저장소의 코드는 [MIT License](LICENSE) 하에 공개됩니다.  
