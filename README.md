# Hi, I'm Myrat 👋

Welcome to my GitHub profile! I'm a **backend developer** who loves building **distributed systems**, **real‑time services**, and **clean, testable backend architectures**. I work extensively with **Go**, **Python/Django**, **Docker**, **Kafka**, and **microservices design**.

---

## 🚀 Current Projects

### 🧩 **Distributed Cart & Stock System (Go + gRPC + Kafka)**
- Services: `cart-service`, `stock-service`, `metrics-consumer`
- Fully gRPC‑based communication with **grpc-gateway**
- Kafka metrics pipeline (topic `metrics`, multi‑partition, RF=2)
- Dockerized multi‑broker Kafka setup
- Robust integration tests using real containers (no mocks)

### 🎧 **Audio Conversion Microservice (Go + FFmpeg)**
- Audio stored in MinIO
- Converts audio → HLS (`.m3u8`, `.ts`)
- Streams at 64kbps / 128kbps / 320kbps
- Built for speed + low resource usage

---

## 🛠️ Technologies & Tools

**Backend:**
- Go (gRPC, Gin, testing, decorators, filters)
- Python (Django, DRF, FastAPI)
- PHP (Laravel) — experience building REST APIs and background workers
- FFmpeg (audio/video processing)
- Redis / RabbitMQ (message brokers)
- Databases: PostgreSQL, MySQL — schema design, migrations, and replication

**DevOps:**
- Docker & Docker Compose
- MinIO (object storage)
- Nginx (reverse proxy)
- CI/CD pipelines

---

## 🧪 Testing Philosophy
- Prefer **real integration tests** over mocks
- Docker‑based test environments (`.env.test`)
- End‑to‑end workflows tested for:
  - Cart service (Add, Delete, List, Clear)
  - Stock service (AddStock, DeleteStock, Get, ListByLocation)

---

## 📚 Featured Code Snippets
```go
// Example: gRPC-based stock fetching
res, err := client.GetStock(ctx, &pb.GetStockRequest{Id: id})
if err != nil {
    t.Fatalf("failed to fetch stock: %v", err)
}
```

```python
# Example: Clean Django validator
@staticmethod
def detach_media(contents, instance):
    ContentAttachment.objects.filter(
        content__in=contents,
        content_type=ContentType.objects.get_for_model(instance),
        object_id=instance.pk,
    ).delete()
```

---

## 🌱 What I'm Learning / Improving
- High-throughput message systems
- Advanced Kafka patterns
- Better FFmpeg pipelines for audio processing
- Distributed caching & performance strategies

---

## 📫 Contact
If you'd like to collaborate or discuss system design, feel free to reach out!

**Thanks for visiting! ⭐**
