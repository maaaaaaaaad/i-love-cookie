# Simple test to create cookie

1. Server: Nest.js
2. Front: React.js

<span style="color:#dc143c">CORS issue</span>

- server

```javascript
app.enableCors({
  credentials: true,
  origin: "http://localhost:3000",
});
```

- client

```javascript
import axios from "axios";

export default class GetMainCookie {
  //
  async getMain() {
    return await axios({
      method: "get",
      url: "http://localhost:5000",
      withCredentials: true, // 👈🏻 important!
    });
  }
}
```
