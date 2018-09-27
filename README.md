# Docker Image for tasksh (Taskwarrior Shell)
This image just installs tasksh out of Ubuntu repositories.
It includes a default `.taskrc`, which sets the data directory to `/root/.task`.

## Basic Run
The most basic run just specifies how the volume for the data (default: `/root/.task`) is loaded:
```
docker run -it --rm -v/your/task/directory:/root/.task ulukai/tasksh
```

## More Configuration
You can override the configuration file at `/root/.taskrc` and, therefore, customize your tasksh:
```
docker run -it --rm -v/your/task/directory:/root/.task -v/your/taskrc:/root/.taskrc ulukai/tasksh
```
