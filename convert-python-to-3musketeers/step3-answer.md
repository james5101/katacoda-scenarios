```yaml
version: '3'
services:
  printvars:
    build: .
    image: printvars-compose:latest
    environment:
        - DOG=HUSKY
```