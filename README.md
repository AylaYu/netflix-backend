# Netflix Backend (mock API)

A small Ktor server that provides fake data for the Netflix Android client. All data is held in memory.

## Endpoints
| Method | Path | Description |
|---|---|---|
| GET | `/home` | Featured video and sections |
| POST | `/videoDetail` | Body `{"id": "squid-game"}` → video and episodes |
| GET | `/profile` | Profile and recently viewed videos |
| GET | `/media/*.mp4` | Sample videos used by the player |

Every request is delayed by 300–500 ms to simulate network latency.

## Tech stack
Kotlin · Ktor (Netty) · kotlinx.serialization

## Run
Use JDK 21.
```bash
./gradlew run
curl localhost:8080/home
```
Server listens on `0.0.0.0:8080`.
