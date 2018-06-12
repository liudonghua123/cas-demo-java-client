# cas demo java client

# run

* edit `src\main\resources\application.properties` to match your cas server.

    The default cas server is localhost on port 8080 and this web app is run on port 9080.
    ```
    server.port=9080

    cas.login.url=http://localhost:8080/cas/login
    cas.url.prefix=http://localhost:8080/cas
    app.server.name=http://localhost
    ```
* execute ```mvn spring-boot:run```
* browse ```http://localhost:9080```, it will redirect to ```http://localhost:8080/cas/login``` for authentication
* see the `attributes` returned from cas server
* edit username field (`attributes.username`) in `src\main\resources\templates\index.html` if needed.

# screenshot

![Screenshot](demo.png?raw=true "Demo")