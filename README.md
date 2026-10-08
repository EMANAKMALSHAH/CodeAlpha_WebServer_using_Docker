Web Server using Docker - CodeAlpha

This project is about deploying a web server inside Docker.

What I did:
- Used Nginx alpine image which is lightweight
- Created Dockerfile with healthcheck
- Added docker-compose for easy management
- Deployed custom index.html website
- Learned container lifecycle commands

How it works:
Build image, run container, open browser on localhost 8080

Commands learned:
docker build, docker run, docker ps, docker logs, docker exec, docker stop, start, restart, rm

Health monitoring is added to check if web server is running fine.

Author: Eman Akmal Shah
CodeAlpha DevOps Intern

On Fri, Oct 9, 2026, 1:59 AM Eman Akmal shah <emanakmalshah@gmail.com> wrote:
name: Java CI with Gradle
on:
  push:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
    - name: Setup Gradle
      uses: gradle/actions/setup-gradle@v3
    - name: Build with Gradle
      run: gradle build


On Fri, Oct 9, 2026, 1:53 AM Eman Akmal shah <emanakmalshah@gmail.com> wrote:
name: Java CI with Gradle
on:
  push:
    branches: [ "main" ]
  pull_request:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - uses: actions/checkout@v4
    - name: Set up JDK 17
      uses: actions/setup-java@v4
      with:
        java-version: '17'
        distribution: 'temurin'
    - name: Setup Gradle
      uses: gradle/actions/setup-gradle@v3
    - name: Build with Gradle
      run: gradle build
