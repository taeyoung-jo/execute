### 💻 Server dockerfile 실행

```
docker build -t ghcr.io/[github 아이디]/[client repo 이미지 이름]:latest .
```

<br />

### 🙆‍♀️ Client dockerfile 실행

client repoisotry에 있던 `.env`에 있던 것들은 `--build-arg`로 전달

Nginx를 이용한 프록시 설정을 했으므로 Server API에 대한 경로는 `/api`로만 작성하면 됨

```
docker build -t ghcr.io/[github 아이디]/[client repo 이미지 이름]:latest --build-arg VITE_SERVER_API_URL=/api .
```

<br />

### 🐳 `.env`와 `docker-compose.yml` 파일을 함께 둔 상태에서 다음 명령어 실행

```
docker compose up -d
```
