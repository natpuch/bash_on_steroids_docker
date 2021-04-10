# bash on steroids docker

Docker container for [bash on steroids](https://github.com/tinoschroeter/bash_on_steroids).

# Usage

Place your `htsh` file in an `html` folder. All variables beginning with `PASS_` will be accessible from `htsh` files.

```yaml
version: "3.4"
services:
  bash_on_steroids:
    container_name: bash_on_steroids
    image: zpex/bash_on_steroids
    environment:
      - TZ=Europe/Paris
      - PASS_var=var_value
    ports:
      - 80:80
    volumes:
        - ./html/:/var/www/html/
```
