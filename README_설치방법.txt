Study Camera — 설치 및 테스트 안내
================================

목표: 광고 없이 문제 사진을 촬영하고 사진의 글씨 선명도와 촬영음을 확인할 수 있는 무료 웹앱.

구성 파일 (5개, 전부 업로드)
- index.html : 앱 화면과 동작 코드
- manifest.webmanifest : 홈 화면에 앱처럼 표시되는 설정
- sw.js : 기본 오프라인 사용을 위한 파일
- icon-192.png / icon-512.png : 앱 아이콘

[무료 게시 방법: 윈도우 PC + GitHub Pages]
1. https://github.com 에서 계정을 만들고 로그인합니다.
2. 오른쪽 위 '+' → New repository 를 누릅니다.
3. Repository name에 study-camera를 입력하고 Public을 선택한 뒤 Create repository를 누릅니다.
4. 저장소에서 uploading an existing file 또는 Add file → Upload files를 엽니다.
5. 이 폴더 안의 index.html, manifest.webmanifest, sw.js, icon-192.png, icon-512.png를 모두 업로드합니다.
6. Commit changes 버튼을 눌러 저장합니다.
7. Settings → Pages → Build and deployment → Source: Deploy from a branch.
8. Branch에서 main / (root)를 선택하고 Save를 누릅니다.
9. Pages 화면에 생성되는 Visit site 링크로 접속합니다.
   보통 https://사용자명.github.io/study-camera/ 형식입니다.
10. 아이폰 Safari에서 해당 주소를 열어 '카메라 시작'을 눌러 권한을 허용합니다.

[아이폰 홈 화면에 앱 추가]
Safari 페이지 메뉴 → 공유 → 홈 화면에 추가 → '웹앱으로 열기' 활성화 → 추가.
(iOS 버전에 따라 메뉴 이름이나 위치가 다를 수 있습니다.)

[테스트 포인트]
1. 책상 위 A4 한 장에 있는 작은 글씨가 선명하게 보이는가?
2. 화면에 표시된 영상 해상도와 촬영 완료 해상도는 얼마인가?
3. 촬영 시 실제 아이폰에서 소리가 발생하는가? (기종/지역/OS별 보장 불가)
4. 사진 저장·공유 버튼을 눌러 iOS 공유 메뉴에서 이미지 저장이 되는가?
5. 사진 공유 메뉴에 ChatGPT가 보이는가? (기기에 설치된 앱 설정에 따라 다름)

[촬영 방식]
- 영상 프레임 (기본): 카메라 동영상에서 프레임을 JPEG 사진으로 변환합니다.
  코드에 셔터음은 없습니다. 하지만 기기/지역의 촬영음 정책을 보장하지는 못합니다.
- 고해상도 실험: 브라우저에서 ImageCapture를 지원하는 경우만 활성화됩니다.
  사진 화질이 향상될 수 있으나 촬영음이 발생할 수 있습니다.

[중요 제한]
- 카메라 접근은 일반적으로 HTTPS 또는 localhost 환경에서 가능합니다.
- Windows에서 HTML 파일을 단순 더블클릭해 여는 방식은 브라우저에 따라 카메라가 안 될 수 있습니다.
- '사진 저장·공유'는 iPhone에서 공유 메뉴를 엽니다. 사진 앱에 자동 저장되는 기능은 아닙니다.
  공유 메뉴에서 '이미지 저장'을 선택하세요. '파일로 저장'은 다운로드 파일 저장입니다.
- 파일은 기본적으로 기기 내에서 처리되며 별도 이미지 업로드 서버가 없습니다.
- GitHub Pages의 public 저장소 코드는 누구나 볼 수 있지만 사용자가 찍은 사진은 그 저장소에 업로드되지 않습니다.
- 무료 GitHub Pages와 Safari 정책은 변경될 수 있습니다.

[변경 방법]
텍스트 편집기로 index.html을 수정한 후 같은 파일을 GitHub에 다시 업로드하세요.
웹앱을 열었을 때 업데이트가 늦으면 Safari 새로고침 또는 앱을 닫았다 다시 열어주세요.
