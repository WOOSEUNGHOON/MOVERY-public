# MOVERY

MOVERY is a tool for discovering modified vulnerable code clones.
Principles and experimental results are discussed in our paper, which will be published in
31st USENIX Security Symposium (Security 2022).

Owing to code refactoring issues, you can currently only test the results of the target programs listed in the paper. We will update the code to apply MOVERY to other software as soon as possible.

## How to use
You can test [MOVERY](https://hub.docker.com/r/seunghoonwoo/movery-public) using Docker:
```
$ sudo docker run -it seunghoonwoo/movery-public:latest
# cd /home/MOVERY
# python3 Detector.py TARGET_PROGRAM
(e.g., python3 Detector.py redis)
```

Currently, there are 10 target programs that can detect vulnerabilities:
'arangodb', 'crown', 'emscripten', 'ffmpeg', 'freebsd-src', 'git', 'opencv', 'openMVG', 'reactos', 'redis'.

### About
This repository is authored and maintained by Seunghoon Woo.

For reporting bugs, you can submit an issue to [the GitHub repository](https://github.com/WOOSEUNGHOON/MOVERY-public) or send me an email (<seunghoonwoo@korea.ac.kr>).
