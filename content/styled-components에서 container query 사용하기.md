---
publish: true
---

# styled-components에서 container query 사용

2024년 10월 15일 기준 `styled-components`최신버전인 `6.1.13` 버전에서도 `Container Query`를 공식적으로 지원 하지 않는다.

- [ ] **컨테이너 쿼리(Container Queries)** 는 CSS의 강력한 기능 중 하나로, 요소의 스타일을 **부모 컨테이너의 크기** 또는 특정 속성을 기준으로 동적으로 조정할 수 있게 해줍니다. 이는 기존의 **미디어 쿼리(Media Queries)** 가 뷰포트(Viewport)의 크기를 기준으로 반응형 디자인을 구현하는 방식과는 차별화된 접근법을 제공

## 지원 브라우저

이미 대부분의 브라우저는 지원을 하고 있기 때문에 사용 하는데 문제가 없으나 styled-components는 아직 지원을 하고 있지 않다.
![[Pasted image 20241015122238.png|Pasted image 20241015122238.png]]

> Container Query 지원 브라우저 버전
> https://caniuse.com/css-container-queries


## 해결

styled-components는 내부적으로 `stylis`를 사용하여 구문 해석을 한다.

현재 styled-components가 사용중인 `stylis`버전은 Container Query를 지원 하지 않는 버전을 사용 중이다.

따라서 임의로 내 패키지에 `stylis`최신 버전을 설치하면 문제없이 Container Query 구문을 해석한다.

공식적으로 지원하진 않기때문에 vscode-styled-components 확장 프로그램에서 경고를 보여주기는 한다.
![[Pasted image 20241015122654.png|Pasted image 20241015122654.png]]


> 참고자료
> https://github.com/styled-components/styled-components/issues/3763