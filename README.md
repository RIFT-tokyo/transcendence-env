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

### 3. Make local .env
```
cp example.env .env
sed -i '' '/FORTYTWO_APP_ID=/s/$/<YOUR_APP_ID_HERE>/g' .env
sed -i '' '/FORTYTWO_APP_SECRET=/s/$/<YOUR_SECRET_KEY_HERE>/g' .env
```

### 4. Build environments by docker compose
```
docker compose up -d
```

### 5. Migration
#### First migration
```
docker compose exec api yarn migration:run
```
