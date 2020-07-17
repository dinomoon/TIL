# Fetch

유튜브 클론 코딩 챌린지를 하면서 알게 되었다.
<br><br>오늘은 공부가 너무 하기 싫어서 대충 했지만...
<br><br>fetch 라는건 데이터를 가져오는 행위를 하는 것 같다.

### 과제 수행 코드 (사용자의 위치를 알려주기)

fetch를 사용해 API_URL에서 위치 정보를 가져온 뒤, html에 넣어준다.

```js
const API_URL = "http://ip-api.com/json/";
const LOCATION = document.querySelector(".location");

fetch(API_URL)
  .then((response) => response.json())
  .then((commits) => {
    LOCATION.innerHTML = `${commits.city}, ${commits.regionName}, ${commits.country}`;
  });
```
