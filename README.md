# Turtle-CLI Docker Image


## Usage

docker run -v $(pwd)/app-release.json:/app/app.json \
-v /opt/jks/cert-1:/certs --rm \
-v /opt/apps/andoird/release:/data \
-e EXPO_ANDROID_KEYSTORE_PASSWORD=password \
turtle-cli\
turtle build:android --keystore-path=/cert/keystore.jks\
--keystore-alias=alias\
--public-url=http://127.0.0.1:90/android-index.json\
--type apk \
-c /app/app.json
-o /data/app-release.apk
