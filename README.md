# Dark Fairy Tale

네 권의 동화책과 3D 숲 인트로, 각 동화의 여섯 장면·인터랙션·마무리 질문으로 구성된 정적 웹사이트입니다.

## GitHub 업로드

배포 ZIP을 압축 해제한 뒤 **github-ready 폴더 안의 내용 전체**를 저장소 최상위에 올립니다. ZIP 파일 자체를 올리는 방식이 아닙니다. 기존 파일과 폴더는 새 배포본으로 교체합니다.

GitHub Pages를 기존 방식으로 사용하는 경우 Settings → Pages에서 Deploy from a branch, main, / (root)를 선택합니다. 이미 설정되어 있으면 파일 교체 후 배포 완료를 기다리면 됩니다. GitHub에 올린 사이트는 CMD 없이 열립니다.

GitHub Actions를 선택할 수도 있습니다. Settings → Pages에서 GitHub Actions를 선택한 후 Actions → Deploy GitHub Pages → Run workflow를 실행합니다. 이 작업에서는 실제 업로드나 배포를 실행하지 않았습니다.

## 로컬 실행

Node.js 20.11 이상에서 START-FAIRYTALE.cmd를 실행합니다. 또는 node preview-server.cjs를 실행하고 http://127.0.0.1:4174 에 접속합니다. HTML 파일을 더블클릭하면 3D 모델을 불러올 수 없습니다.

## 수정과 배포

npm ci
npm run check
npm run build
npm run release

소스의 이미지와 영상은 최적화되어 있습니다. 배포 폴더는 실제 사용하는 파일만 포함하고 JavaScript와 CSS를 압축합니다. .backups, .tools, node_modules, release, dist, 원본 MOV, 테스트 캡처를 GitHub에 올리지 않습니다.

빨간모자 원본과 최적화 전 미디어는 작업 폴더의 .backups에 별도로 보관됩니다. 웹 배포에는 포함하지 않습니다.

## 구성

- forest-entry: 3D 숲과 나비 인트로
- book-library: 네 권의 책 선택
- tales: 공통 이야기·장면 전환·교훈
- redridinghood / cinderella / snowwhite / mermaid: 동화별 페이지와 삽화
- assets: 투명 배경 파티클 영상

투명 WebM은 VP9, 이미지는 WebP를 사용합니다. 느린 기기에서는 숲의 렌더링 품질이 자동으로 낮아집니다. 브라우저의 움직임 줄이기 설정을 지원합니다.

라이선스는 THIRD_PARTY_NOTICES.md를 참고하세요.
