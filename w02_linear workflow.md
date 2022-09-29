# Linear workflow

### 리니어 워크플로우란?
디지털 데이터가 서로 표현하는 방식이 다 달라서 색 차이가 나기 때문에 모든 그래픽 작업을 선형 색 공간에서 이루는 방식을 말한다.
인간의 눈은 어두운 색에 민감하기 때문에 그림1에서 위쪽 그라데이션이 더욱 정확하게 느껴진다.
그러나 수학적으로 더 정확한 그라데이션은 아래쪽 것이다.   
<img src="https://user-images.githubusercontent.com/60923302/118788622-ecc46600-b8ce-11eb-843c-c985eb6be98e.png" width="600px" height="300px">

이렇듯 리니어 컬러 스페이스의 그라데이션을 감마 컬러 스페이스의 그라데이션처럼 자연스럽게 만들기 위해서는 아래 그래프처럼 감마값을 조정해야한다. 
우리가 빛보다 어두운 부분을 더 많이 볼 수 있기 때문에 어두운 부분에 비트를 더 많이 사용하여 밝기를 낯주는 것을 
감마 인코딩이라 하는데 이렇게 저장된 이미지는 원본보다 훨씬 어두워진 채 저장되는 것이다.

<img src="https://user-images.githubusercontent.com/60923302/118791046-4b8adf00-b8d1-11eb-9356-6708af7bb7da.png" width="450px" height="450px"> <img src="http://www.puredevsoftware.com/blog_images/gamma_encoded_values.png" width="500px" height="200px">

그림3- 밝기 값이 8비트로 인코딩되는 방법
어둡게 저장된 이미지를 다시 원본사진처럼 출력하기 위해서 jpeg와 같은 이미지 파일들은 자체적으로 감마보정, 즉 밝아진 채로 저장이 된다. 그렇게 되면 밝게 저장된 이미지를 감마 인코딩을 통해 어둡게 만들어 결과적으로 원본과 같은 이미지를 출력할 수 있게 되는 것이다.   
<img src="https://user-images.githubusercontent.com/60923302/118792515-af61d780-b8d2-11eb-83fc-acc6de68c077.png" width="600px" height="250px">

이러한 감마값의 보정은 crt 모니터에서도 이루어졌는데, crt 모니터가 이미지를 어둡게 출력하는 문제 때문에 감마 보정을 통해 원본과 같은 색상으로 만드는 sRGB 방식이 도입되었다.


출처: https://www.puredevsoftware.com/blog/2019/01/21/gamma-encoding/#:~:text=Gamma%20encoding%20is%20a%20non-linear%20mapping%20To%20map,usually%20be%20stored%20as%20a%20gamma%20encoded%20image.
https://kyoungwhankim.github.io/ko/blog/color_linearworkflow/#:~:text=%EC%84%A0%ED%98%95%20%EC%9B%8C%ED%81%AC%ED%94%8C%EB%A1%9C%EC%9A%B0(Linear%20Workflow)%2C%20%ED%98%B9%EC%9D%80%20%EB%A6%AC%EB%8B%88%EC%96%B4%20%EC%9B%8C%ED%81%AC%ED%94%8C%EB%A1%9C%EC%9A%B0,%EC%97%90%EC%84%9C%20%EC%9D%B4%EB%A3%A8%EC%96%B4%EC%A7%80%EB%8A%94%20%EB%B0%A9%EC%8B%9D%EC%9D%84%20%EB%A7%90%ED%95%A9%EB%8B%88%EB%8B%A4.
https://chrisbrejon.com/cg-cinematography/chapter-1-5-academy-color-encoding-system-aces/
