# cas demo java client

# run

- edit `src\main\resources\application.properties` to match your cas server.

  The ynu cas server is http://ids.ynu.edu.cn and this cas client is run on http://127.0.0.1:8080.

  ```
  server.port=8080

  cas.login.url=http://ids.ynu.edu.cn/authserver/login
  cas.url.prefix=http://ids.ynu.edu.cn/authserver
  app.server.name=http://127.0.0.1:8080
  ```

- execute `mvn spring-boot:run`
- browse `http://127.0.0.1:8080`, it will redirect to `http://ids.ynu.edu.cn/authserver/login` for authentication
- see the `attributes` returned from cas server
- edit uid field (`attributes.uid`) in `src\main\resources\templates\index.html` if needed.

# screenshot

![Screenshot](demo.png?raw=true 'Demo')
