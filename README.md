# app-updates

`sejongfnc-code` 계정에 만든 **앱 자동 업데이트 전용 단일 저장소**입니다.
정지된 `hsm20001026-create` 계정의 앱별 `*-updates` 저장소를 여기로 모았습니다.
저장소는 하나만 쓰고, APK는 이 저장소의 GitHub Release 자산으로만 올립니다.

## URL 규칙 (새 주소)

기본 Pages:

- latest.json: `https://sejongfnc-code.github.io/app-updates/<app>/latest.json`
- raw 백업: `https://raw.githubusercontent.com/sejongfnc-code/app-updates/main/<app>/latest.json`
- APK: `https://github.com/sejongfnc-code/app-updates/releases/download/<app>-v<versionName>/<filename>.apk`

`<app>` 폴더 이름은 아래 표의 slug입니다. 앱 소스의 업데이트 URL은 각 앱 폴더 도우미가 바꿉니다.

`releases/latest/download/latest.json` 은 이 저장소에서 쓰면 안 됩니다. 저장소 전체의 "latest" 릴리스가 하나뿐이라 앱이 여러 개일 때 섞입니다.

## 예전 주소 (비교)

- latest.json (주로): `https://raw.githubusercontent.com/hsm20001026-create/<app>-updates/main/latest.json`
- 또는: `https://github.com/hsm20001026-create/<app>-updates/releases/latest/download/latest.json`
- APK: `https://github.com/hsm20001026-create/<app>-updates/releases/download/v<versionName>/<filename>.apk`

## latest.json 필드

`versionCode`, `versionName`, `apkUrl`(https만), `sha256`, `notes`, `size`

앱은 열려 있을 때만 확인하고, sha256·패키지·서명 검증 뒤에 설치합니다 (공메 33).

## 이미 설치된 폰

이미 깔린 앱은 예전 주소를 보고 있으므로, 새 주소를 가리키는 빌드를 **한 번 수동 설치**해야 이후 자동 업데이트가 됩니다.
