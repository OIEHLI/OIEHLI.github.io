# Merry GYURISMAS! — OIEHLI

프로미스나인 장규리의 생일을 축하하기 위해 사진과 메시지를 배치한 정적 팬 웹페이지입니다.

## 목적과 주요 기능

사진을 캡션과 함께 둘러보고 생일 축하 분위기를 전달하는 화면입니다. [index.html](index.html)에 사진 갤러리와 포스트잇 모양 메시지를 배치하고, [js/index.js](js/index.js)에서 Magnific Popup 이미지 뷰어를 연결합니다.

- 사진·캡션 목록과 CSS 갤러리 배치
- 데스크톱 이미지 확대와 갤러리 이동
- 포스트잇 스타일의 정적 메시지 영역

메시지는 HTML에 미리 적힌 샘플입니다. 방문자가 메시지를 작성·제출·저장하는 기능과 백엔드·데이터베이스는 없습니다.

## 실제 화면과 데모

[공개 페이지](https://oiehli.github.io/)에서 갤러리를 볼 수 있습니다. 2026-11-13 Chrome에서 본문 렌더링을 확인했습니다. 확대 뷰어는 코드상 화면 너비 640px 미만에서 비활성화됩니다.

## 기술 스택과 구조

- HTML, CSS, JavaScript
- jQuery 3.2.1, Magnific Popup 1.1.0, Modernizr, 외부 웹폰트
- GitHub Pages 정적 호스팅

사진·본문은 [index.html](index.html), 갤러리 스타일은 [css/style.css](css/style.css), 포스트잇 스타일은 [css/postit.css](css/postit.css)에 있습니다. 완성된 HTML/CSS/JS를 직접 제공하는 구조여서 별도 서버 애플리케이션이 필요하지 않습니다.

[index.haml](index.haml), [CoffeeScript 소스](coffeescript/index.coffeescript), [Sass 소스](sass/style.sass)도 있지만 자동 빌드 설정은 없습니다. 이 파일들을 수정한다고 현재 제공되는 HTML/CSS/JS가 자동으로 바뀌지는 않습니다.

## 로컬 실행

Python 3이 설치되어 있다면 다음과 같이 엽니다.

```bash
git clone https://github.com/OIEHLI/OIEHLI.github.io.git
cd OIEHLI.github.io
python3 -m http.server 5173 --bind 127.0.0.1
```

`http://127.0.0.1:5173/`에 접속합니다. 외부 라이브러리·폰트 CDN 연결에는 인터넷이 필요합니다.

## 검증과 현재 한계

자동 테스트와 CI 설정은 없습니다. 화면 확인 시 사진 경로·캡션, 넓은 화면의 팝업, 좁은 화면의 배치를 확인해야 합니다.

- 2026-11-13 공개 화면에서 `Unexpected token '>'` 오류를 관찰했습니다. `index.html`이 일반 JavaScript로 불러오는 [js/xgrmnr.js](js/xgrmnr.js)에 `do ->`로 시작하는 CoffeeScript 문법이 남아 있습니다. 현재 화면이 오류 없이 동작한다고 보장할 수 없습니다.
- 포스트잇에는 테스트 문구가 남아 있으며 메시지 수집 기능은 없습니다.
- 외부 CDN과 과거 브라우저 라이브러리에 의존합니다. 전체 상호작용과 모바일 호환성을 다시 검증하지 않았습니다.
- 사진과 참고 코드의 권리는 각 원저작자에게 있습니다. 저장소에 별도 LICENSE 파일은 없습니다.

## 참고한 코드와 출처

기존 README의 참고 출처를 유지합니다.

- [CodePen — mican](https://codepen.io/mican/pen/awxmpY)
- [CodePen — mingabire](https://codepen.io/mingabire/details/BDcIf)

화면의 기존 `© DIRECTORJJUN` 표기와 각 자료의 출처를 유지해야 합니다.
