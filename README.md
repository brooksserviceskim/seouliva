# SEOULIVA — K-Beauty Warehouse · Kenya Proposal (서울리바)

3개국어(한국어 · English · Kiswahili) 웹 제안서.
**제안: Brooks Global · CEO** / 유통 브랜드: SEOULIVA(서울리바) Beauty Warehouse — 독립 K-뷰티 리테일·OEM 유통 사업.

미팅: 2026-06-03 (케냐 바이어). 단일 페이지 정적 사이트(`index.html` + `assets/`). 폰트: Pretendard. 모든 기기(아이폰 SE~데스크톱) 반응형 검증 완료.

---

## 폴더 구조 (파일명 모두 영문)
```
SEOULIVA_Website/
├─ index.html
├─ .nojekyll                  # GitHub Pages 에서 assets 폴더 정상 표시용
├─ README.md
└─ assets/
   ├─ brand/logo.png          # 누끼 로고(투명 배경)
   ├─ store/                  # 매장 사진 (jpg, 가볍게 압축)
   │   exterior.jpg · interior1.jpg · interior2.jpg · counter.jpg
   │   signage.jpg · uniform.jpg · apron.jpg
   └─ product/                # 제품 이미지 (png, 투명 배경)
       serum.png · cream.png · sunscreen.png · toner.png · tonerpad.png · mask.png
```
외부 의존성은 Pretendard 폰트·Chart.js(CDN)뿐. 인터넷만 되면 바로 열립니다. 전체 약 1.4MB.

> 데스크톱 폴더에 압축본 **`SEOULIVA_Website_GitHub.zip`** 도 함께 만들어 두었습니다. Netlify Drop이나 압축 업로드에 쓰면 편합니다.

## 로컬 미리보기
`index.html` 더블클릭 → 브라우저로 열기. 우상단 **한국어 / EN / SW** 버튼으로 언어 전환.

---

## GitHub Pages 업로드 (드래그앤드롭, 가장 쉬움)
1. https://github.com 로그인 → 우측 상단 **+** → **New repository**.
2. Repository name 예: `seouliva-kenya` → **Public** → **Create repository**.
3. 새 저장소 화면에서 **uploading an existing file** 링크 클릭.
4. **`SEOULIVA_Website` 폴더 안의 내용물**(`index.html`, `.nojekyll`, `README.md`, `assets` 폴더)을 통째로 드래그해 업로드.
   - ⚠️ 폴더 자체가 아니라 **그 안의 파일들**을 올려야 `index.html`이 최상위에 옵니다.
   - `.nojekyll` 파일도 꼭 함께 올려주세요(이미지가 안 나오는 문제 예방).
5. **Commit changes** 클릭.
6. 상단 **Settings → Pages**.
7. **Source**: `Deploy from a branch` → **Branch**: `main` / `/ (root)` → **Save**.
8. 1~2분 뒤 주소가 표시됩니다: `https://<아이디>.github.io/seouliva-kenya/`
   → 이 링크를 케냐 바이어에게 공유.

## (대안) 계정 없이 즉시 — Netlify Drop
https://app.netlify.com/drop 에 `SEOULIVA_Website` 폴더(또는 zip)를 드래그 → 바로 공개 링크 생성.

## (대안) Git 명령어
```bash
cd "SEOULIVA_Website"
git init && git add . && git commit -m "SEOULIVA Kenya proposal"
git branch -M main
git remote add origin https://github.com/<아이디>/seouliva-kenya.git
git push -u origin main
# 이후 Settings → Pages 에서 main / root 게시
```

---

## 수정 팁
- 텍스트: `index.html` 하단 `I18N = { ko / en / sw }` 객체에서 언어별 수정.
- 차트 숫자: `makeCharts()` 함수의 각 `data:[...]` 배열.
- 가격/투자/손익표: 본문 `<table>` 셀 값 직접 수정.
- 시장 수치 출처는 페이지 하단 Sources. 재무 수치는 "예시 추정치(현지 검증 필요)"로 표기됨.
