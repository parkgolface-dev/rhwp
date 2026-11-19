# DocPrism 포크 (docprism 가지)

DocPrism 안드로이드 문서뷰어(com.pagcode.docprism)가 쓰는 rhwp 판입니다. 원 저장소는 edwardkim/rhwp (MIT) 입니다.

- **가지:** `docprism` — 원 저장소 릴리스 태그(vX.Y.Z)를 합치고, DocPrism 전용 패치를 그 위에 커밋합니다.
- **빌드:** `sh scripts/wasm-pack-locked.sh --target web --release --out-dir target/docprism-pkg -- --no-default-features --features console_error_panic_hook,wasm-api`
  - PDF 가져오기(pdf-import·jbig2·jpeg2000·icc)를 빼서 wasm 이 27.9MB → 19.2MB 로 줄어듭니다.
- **자동 갱신:** DocPrism 저장소의 `tool/libs/weekly.sh` 가 매주 목요일 05:00 에 새 태그를 합치고, 회귀 시험을 통과하면 이 가지를 올립니다.
- 원 저장소에 도움이 되는 수정은 별도 가지로 원 저장소에 PR 을 보냅니다.
