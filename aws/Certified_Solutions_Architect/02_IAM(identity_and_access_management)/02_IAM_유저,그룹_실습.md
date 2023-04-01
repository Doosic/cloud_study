# IAM 유저,그룹 실습

- AWS 콘솔에 접속하여 IAM 대시보드로 이동한다.

## 암호 정책 변경
- 왼쪽 탭의 계정 설정으로 이동하여 암호 정책을 내 변경할 수 있다.
- <img src="https://user-images.githubusercontent.com/82255957/229272879-7a4f52c1-8634-4939-b6b8-712f962de8c4.png" width="400" height="250"/>
- 사용자 지정을 통하여 필요한 정책대로 암호 정책을 만들어 사용하자.

## MFA 설정 (2차 보안인증. 토큰,OTP 등..)
- 루트 계정은 MFA를 설정하여 사용하도록 권장된다.(대시보드에 MFA추가 및 오른쪽 상단의 계정버튼에 보안 자격 증명을 이용하여 설정페이지로 이동이 가능하다.)
- <img src="https://user-images.githubusercontent.com/82255957/229273017-06b4050e-4041-4b8a-82cb-4d83d2df67fa.png" width="400" height="250"/>
- <img src="https://user-images.githubusercontent.com/82255957/229273079-309d0994-9e0b-4f24-b7b6-61476853c4f5.png" width="400" height="250"/>
- IAM > 보안 자격 증명 페이지로 이동후 멀티 팩터 인증 디바이스 할당(활성화)를 클릭한다.
    - <img src="https://user-images.githubusercontent.com/82255957/229273480-f2704158-a5e9-45a5-ae58-89628e924093.png" width="400" height="250"/> 
    - 1.인증 관리자 앱은 구글 또는 MicroSoft 사의 OTP를 만들어주는 서비스를 연동하여 로그인할 때 사용한다.
    - 2.보안키는 물리적인 보안키이다.
    - 3.하드웨어 TOTP 토큰은 은행같은 곳에서 사용하는 보안 토큰을 사용하는 것이다.

## 사용자 추가
- <img src="https://user-images.githubusercontent.com/82255957/229273571-9ce1cd79-1931-42e4-aaae-e5b2dcaff895.png" width="400" height="250"/>
- <img src="https://user-images.githubusercontent.com/82255957/229273943-498c262c-0392-465d-883a-51faa8099167.png" width="400" height="250"/>
- 사용자를 그룹별로 분류하여 직무별로 사용자 권한을 관리한다. (실습이기에 전체 권한을 부여.)
- <img src="https://user-images.githubusercontent.com/82255957/229274135-e627b7c3-ddd0-4534-a8a3-01ccf148f1f4.png" width="400" height="250"/>
- 만들어진 사용자 정보는 이메일 및 .csv 파일로 받을 수 있다.

## 새로운 계정으로 Access 하기
- 대시보드 > 오른쪽 탭에 해당 계정의 IAM 사용자를 위한 로그인 URL로 이동하여 접속이 가능하고 해당 링크는
  계정 별칭을 변경하며 편집이 가능하다. (별칭은 중복될 수 없다.)
- <img src="https://user-images.githubusercontent.com/82255957/229274785-10ef8b47-66cf-4c2a-b9cd-325270997a9b.png" width="400" height="250"/>
- 링크로 이동하여 로그인시 다음과 같이 IAM사용자 라고 표기된다.
- <img src="https://user-images.githubusercontent.com/82255957/229275036-2e413e79-c0f7-429e-9b1e-9d7fe6d51ec7.png" width="400" height="250"/>
- <img src="https://user-images.githubusercontent.com/82255957/229274895-c9c5d78f-7b91-4507-805f-f34bfd032a44.png" width="400" height="250"/>
