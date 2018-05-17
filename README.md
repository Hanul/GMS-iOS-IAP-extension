# GMS-iOS-IAP-extension
모바일 환경에서는 인 앱 결제 도중 앱이 종료(정확히 말하면 Consume하기 전)되는 경우, 다음번에 앱이 실행될 때 결제 내역을 자동으로 복구하려 시도합니다.

그런데 GameMaker: Studio로 만든 프로젝트의 경우 iOS에서 결제 내역을 복구하려 할 때 튕기는 버그가 있습니다. 문제는 버그가 발생한 이후부터 계속해서 튕긴다는 사실입니다. (계속 복구하려 하기 때문) 이를 고치기 위해서는 무조건 앱을 삭제했다가 다시 깔아야 하는데요, 이 과정에서 유저 이탈률이 높을 수 밖에 없습니다.

`GMS-iOS-IAP-extension`는 이런 문제를 회피하고자 iOS의 전체 인 앱 결제 과정을 자체 개발한 익스텐션입니다.

## 설치 방법
Extensions에서 `iOS-IAP.gmez`를 Import 합니다. 이후 익스텐션을 열어 `Import Resources` 탭을 간 후, `Import All`을 눌러 모든 리소스를 임포트합니다.

## 사용 방법
아래와 같은 네가지 함수가 있습니다. GMS 자체 인앱 결제 함수들과 형태가 유사합니다.
* `niap_activate(product_list)` `product_list`에 각 상품의 정보를 추가하여, 인 앱 결제를 활성화합니다.
* `niap_is_available()` 인 앱 결제가 사용 가능한지 확인합니다.
* `niap_acquire(product_id)` 인 앱 결제를 요청합니다.
* `niap_consume(product_id)` 인 앱 결제가 완료되면 요청을 완료합니다.

## 라이센스
[MIT](LICENSE)

## 작성자
[Young Jae Sim](https://github.com/Hanul)
