<img src="https://raw.githubusercontent.com/e-cattle/art/master/eCattle.png" width="200" alt="e-Cattle Logo" />

# Development environment to middleware BigBoxx.

This project will provide the development environment for BigBoxx modules.

## Prerequisites

- Tested and Approved on MacOS and Ubuntu Linux Operation Systems;
- Docker and docker-compose: **https://docs.docker.com/get-docker/** and **https://docs.docker.com/compose/install/** ;
- GIT;
- NodeJS v12.16.2;
- NodeJS dependency managers **yarn** or **npm**.

## Instructions

### Step 01: Create workspace and run git clone of projects.

- The suggested folder name for the project's workspace is **bigboxx**.

```shell
~$ mkdir bigboxx
~$ cd bigboxx
~/bigboxx$ git clone https://github.com/e-cattle/middleware.git
~/bigboxx$ git clone https://github.com/e-cattle/install.git
~/bigboxx$ git clone https://github.com/e-cattle/kernel.git
~/bigboxx$ git clone https://github.com/e-cattle/query.git
~/bigboxx$ git clone https://github.com/e-cattle/totem.git
~/bigboxx$ git clone https://github.com/e-cattle/lora.git
```

### Step 02: Download NodeJS dependencies for BigBoxx modules

- It is necessary to access the folders of all projects to download the dependencies. 

- **Module Kernel**
```shell
# Option: 01 - Using Yarn
~/bigboxx/kernel$ yarn install
# Option: 02 - Unsing npm
~/bigboxx/kernel$ npm i
```

- **Module Query**
```shell
# Option: 01 - Using Yarn
~/bigboxx/query$ yarn install
# Option: 02 - Unsing npm
~/bigboxx/query$ npm i
```

- **Module Totem**
```shell
# Option: 01 - Using Yarn
~/bigboxx/totem$ yarn install
# Option: 02 - Unsing npm
~/bigboxx/totem$ npm i
```

- **Module Lora**
```shell
# Option: 01 - Using Yarn
~/bigboxx/lora$ yarn install
# Option: 02 - Unsing npm
~/bigboxx/lora$ npm i
```

### Step 03: Building containers of BigBoxx modules with docker-compose

- The middleware project contains the files **docker-compose.yml** and **docker-compose.override.yml** that are responsible for generating and starting the containers for maintenance and development of the bigboxx modules.
- The **docker-compose** will access the *Dockerfiles* of each module to generate the images. 

```shell
# Run only the first time. In the next executions the parameter --build is not necessary.
~/bigboxx/middleware$ docker-compose up --build
```

