```
version: '3'
services:
  printvars:
    build: .
    image: printvars:latest
    environment:
        - DOG=HUSKY
```    