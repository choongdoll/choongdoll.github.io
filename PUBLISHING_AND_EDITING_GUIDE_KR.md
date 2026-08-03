# GitHub Pages 게시 및 수정 가이드

## 1. 처음 게시하기

1. GitHub에 `choongdoll` 계정으로 로그인합니다.
2. 새 repository를 만들고 이름을 정확히 `choongdoll.github.io`로 입력합니다.
3. Public을 선택하고, README / .gitignore / license는 추가하지 않은 빈 repository로 생성합니다.
4. 이 ZIP을 압축 해제합니다.
5. 압축 해제한 폴더 안의 모든 항목(`index.html`, `assets` 폴더, `404.html`, `.nojekyll` 등)을 repository 최상위에 업로드합니다.
   - ZIP 파일 자체를 업로드하지 않습니다.
   - 바깥 폴더 하나만 올리지 말고, `index.html`이 repository 첫 화면에 바로 보여야 합니다.
6. Commit message에 `Publish website`라고 적고 main branch에 commit합니다.
7. repository의 `Settings → Pages`로 이동합니다.
8. `Source: Deploy from a branch`, `Branch: main`, `Folder: /(root)`를 선택하고 Save합니다.
9. 게시가 끝나면 `https://choongdoll.github.io`에서 확인합니다.

## 2. 문구 수정하기

대부분의 문구는 `index.html` 한 파일에 있습니다.

1. repository에서 `index.html`을 클릭합니다.
2. 오른쪽 위 연필 아이콘(Edit this file)을 클릭합니다.
3. Ctrl+F로 바꾸고 싶은 기존 문구를 검색합니다.
4. HTML 태그는 그대로 두고, `>`와 `<` 사이의 영어 문구만 바꿉니다.
5. `Commit changes...`를 클릭하고 main branch에 commit합니다.
6. 잠시 뒤 홈페이지에 자동 반영됩니다.

예시:

```html
<p class="hero-lead">Developing soft, implantable, and wearable bioelectronic systems...</p>
```

아래처럼 문장 부분만 수정합니다.

```html
<p class="hero-lead">새로 사용할 영문 문장</p>
```

## 3. 파일 위치

- 소개, 연구, 논문, 수상, 연락처 문구: `index.html`
- 글자 크기, 간격, 배경 등 디자인: `assets/styles.css`
- 모바일 메뉴와 스크롤 애니메이션: `assets/script.js`
- 프로필 및 연구 이미지: `assets/images/`

## 4. 링크 수정하기

링크는 `index.html`의 `href="..."` 부분입니다. 따옴표 안의 주소만 바꿉니다.

```html
<a href="새 주소">Google Scholar</a>
```

## 5. 이미지 교체하기

가장 쉬운 방법은 새 이미지의 파일명과 형식을 기존 파일과 동일하게 만든 뒤 `assets/images/`에서 기존 파일을 교체하는 것입니다.

- 프로필 사진: `profile.webp`
- 대표 연구: `implant-system.webp`
- 무선 네트워크 연구: `wireless-network.webp`
- 행동 연구: `behavior-study.webp`

## 6. 수정 시 주의

- `<section>`, `<div>`, `<a>`, `<p>` 같은 태그를 지우지 않습니다.
- `class="..."` 내용은 디자인과 연결되므로 문구 수정 시 건드리지 않습니다.
- 큰 레이아웃 변경 전에는 기존 파일을 별도로 보관합니다.
