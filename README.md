# AndroidDocker
Dockerfile for Android with Kotlin

Docker file for Android with Ubuntu base image, OpenJdk 8, Android SDK and Fastlane.

## Built images are published on Docker Hub:  
https://hub.docker.com/r/bilueandroid/android-kotlin/tags/

## To Publish a new image

1. List the contents of the curent folder on your Mac to make sure you're building an image that contains everything you want.
```
ls -l
	Dockerfile
	README.md
	license_accepter.sh
```

2. Build the image giving it a meaningful name
```
docker build -t android-kotlin .
```

3. Login to Docker Hub - username is bilueandroid. Get password from 1Password.
```
docker login
```

4. Tag the image with a version number (1.2.3. in this case)
```
docker tag android-kotlin bilueandroid/android-kotlin:1.2.3
```

5. Push the image to Docker Hub.
```
docker push bilueandroid/android-kotlin:1.2.3
```

6. Update any pipline.yaml files that may use the image.
```
image: "bilueandroid/android-kotlin:1.2.3"
```
