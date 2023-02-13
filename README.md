## How to develop
### 1. Clone the repository
```
git clone --recurse-submodules -j8 https://github.com/RIFT-tokyo/transcendence-env.git
cd transcendence-env
```

### 2. Make local .env
```
cp example.env .env
sed -i '' '/FORTYTWO_APP_ID=/s/$/<YOUR_APP_ID_HERE>/g' .env
sed -i '' '/FORTYTWO_APP_SECRET=/s/$/<YOUR_SECRET_KEY_HERE>/g' .env
```
###### ※ If you're a 42 student, replace <YOUR_APP_ID_HERE> and <YOUR_SECRET_KEY_HERE> correctly. Otherwise, there is no need to replace them. Run `sed` as is. In that case, you will not be able to use 42 OAuth feature.

### 3. Build environments by docker compose
```
docker compose up -d
```

### 4. Enjoy
Access [http://localhost:4212](http://localhost:4212)
