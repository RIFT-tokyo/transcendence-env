## How to develop
### 1. Clone the repository
```
git clone https://github.com/RIFT-tokyo/transcendence-env.git
```

### 2. Clone other repogitories
```
cd transcendence-env
git clone https://github.com/RIFT-tokyo/transcendence-api.git api
git clone https://github.com/RIFT-tokyo/transcendence-front.git front
git clone https://github.com/RIFT-tokyo/transcendence-docs.git docs
```

### 3. Build environments by docker compose
```
docker compose up -d
```

### 4. Migration
#### First migration
```
docker compose exec api yarn migration:run
```
