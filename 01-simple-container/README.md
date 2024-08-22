## Beginner Docker

**Golang App**

- docker run --rm -v "C:\Users\Mayank-PC\Python-Developer\docker-containers\projects\01-beginner-docker\golang-app:/app" golang:1.16 go run /app/main.go

**Python App**

- docker run --rm -v "C:\Users\Mayank-PC\Python-Developer\docker-containers\projects\01-beginner-docker\python-app:/app" python:3.8-slim python /app/script.py

**Ruby App**

- docker run --rm -v "C:\Users\Mayank-PC\Python-Developer\docker-containers\projects\01-beginner-docker\ruby-app:/app" ruby:3.0 ruby /app/script.rb
