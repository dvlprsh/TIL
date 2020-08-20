# Chrome 80 SameSite cookie issue
> 구글 크롬(Google Chrome) 80 버전부터 `새로운 쿠키 정책`이 적용되어 Cookie의 `SameSite` 속성의 기본값이 `None`에서 `Lax`로 변경되었다.

브라우저에서 기본 설정을 변경한 이유는 크로스 도메인 간 중요한 유지는 CSRF 가능성이 있는 쿠키가 아닌 다른 안전한 방식으로 하기를 권장하기 때문이다.

기존에 잘 작동하던 api가 동작하지 않을 경우 `Chrome 80 cookie issue`를 의심해볼 만하다. 이후 Firefox, Edge 등 다른 브라우저도 Chrome과 동일한 설정으로 기본값을 변경할 예정이라고 한다.

### SameSite 설정하기
당장 쿠키에 대한 의존성을 낮출 수 없는 경우를 위한 임시 해결책이다.
크로스 사이트 간 쿠키를 전송하려면 `SameSite` 속성을 `None`으로 설정해야 하는데, 이때 `Secure` 속성을 추가해 주어야 한다. `Secure` 속성이 추가된 쿠키는 HTTPS 프로토콜에서만 전송이 가능하다.
> SameSite=None; Secure;

(자세한 내용은 아래 자료를 참고하세요.)

---
### 출처
- https://ifuwanna.tistory.com/223
- https://web.dev/samesite-cookies-explained/