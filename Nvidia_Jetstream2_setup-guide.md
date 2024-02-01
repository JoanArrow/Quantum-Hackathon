# Setup Guide
Follow these instructions for setting up and logging into your virtual workstation. 

Any time you see text wrapped by brackets \<LIKE-THIS-TEXT>, that means both text and brackets should be replaced.

## Quickstart
From a terminal on your local machine, ssh into your instance with given IP and enter password
```
ssh exouser@<INSTANCE-IP-ADDRESS-HERE>
```

Download the CUDA quantum docker images
```
docker pull nvcr.io/nvidia/nightly/cuda-quantum:latest
```

Launch the docker container
```
docker run -it --gpus all --name cuda-quantum nvcr.io/nvidia/nightly/cuda-quantum:latest
```

Launch a Visual Studio Code Server. The server name must be unique and less than 20 characters. We recommend using your initials with some numbers(Eg: cq-djh-1234)
```
vscode-setup tunnel --name <UNIQUE-NAME-HERE> --accept-server-license-terms
```

Select `Github Account` and follow instructions to authenticate

Click the link (format: https://vscode.dev/tunnel/<your-server-name-here>) to open VSCode in your browser. Select `Github` again.

Congrats! You are now logged into your VS Code Server and can begin hacking! Make sure to save that url somewhere so you can access it again later!
