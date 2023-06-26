## ETL Pipeline

This repository contain codes on the etl process to extract, load and transform data learned through the bootcamp sessions from waia

### Introduction
Building an ETL pipeline that carries out the following tasks:
- Extracts transactional data from Redshift
- Transforms the data by identifying and removing duplicates, blank customer ids
- Loads the transformed data to s3 bucket

### Requirements
  The minimum requirements:
- Docker for Mac: [Docker >= 20.10.2](https://docs.docker.com/docker-for-mac/install/)
- Docker for Windows: 
  - Installation: [Docker](https://docs.docker.com/desktop/install/windows-install/)
  - Manual installation steps for older WSL version: [Docker WSL 2](https://learn.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package)

### Instructions on how to execute the code
Copy the ``.env.example`` file to `.env` and fill out the environment vars.

Make sure you are executing the code from the etl_pipeline folder and you have Docker Desktop running.

To run it locally first build the image.

```bash
  docker image build -t etl-pipeline:0.1 .
```

Then run the etl job using docker:
```bash
  docker run --env-file .env etl-pipeline:0.1
```
