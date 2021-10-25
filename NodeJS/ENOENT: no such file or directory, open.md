# 에러 시점
- Stream에 대하여 공부하던 중 createWriteStream을 사용했을 때 발생한 에러
```js

  const fs = require("fs");

  const ws = fs.createWriteStream("local/big-file");

```

# 에러 원인
- 부모 경로(local)이 존재하지 않아 파일을 파일 시스템의 root 경로에 쓰려고 해서 발생

# 해결 방법
- 부모 디렉토리를 생성하거나, 현재의 경로(./)에 파일을 생성해준다.
