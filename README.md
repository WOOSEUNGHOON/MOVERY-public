# MOVERY

MOVERY is a tool for discovering modified vulnerable code clones.
Principles and experimental results are discussed in our paper, which will be published in
31st USENIX Security Symposium (Security 2022).

## How to use
**[2023-03-31: NOW IT IS UPDATED]**
You can test [MOVERY](https://hub.docker.com/r/seunghoonwoo/movery-public) using Docker.
All the datasets used in MOVERY and the source code of the detector are contained in the Docker image.

### 1. Execute MOVERY-Docker
```
$ sudo docker run -it seunghoonwoo/movery-public:latest
# cd /home/MOVERY
```

### 2. Prepare testing repository
Suppose we want to scan the "redis" repository.
```
# git clone https://github.com/redis/redis
```
Now "/home/MOVERY/redis" is prepared.

### 3. Run preprocessor
```
# python3 Preprocessor.py TARGET_PROGRAM
(e.g., python3 Preprocessor.py redis)
```
This may take several minutes depending on the code size.

### 4. Run Detector
```
# python3 Detector.py TARGET_PROGRAM 0
(e.g., python3 Detector.py redis 0)
```
The vulnerability detection result will be printed.

### FAQ

- You can check vulnerability and patch datasets from Docker.
- A patch signature only considers code lines that are not included in the respective vulnerability signature. 

### About
This repository is authored and maintained by Seunghoon Woo.

For reporting bugs, you can submit an issue to [the GitHub repository](https://github.com/WOOSEUNGHOON/MOVERY-public) or send me an email (<seunghoonwoo@korea.ac.kr>).
