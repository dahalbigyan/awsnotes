1. Get Docker Community Edition(CE) for Mac
    - Install Docker.dmg
2. Start Docker
    - docker version
    - docker run hello-world
        -- Docker client contacts Docker daemon
              -- Docker daemon pulls the "hello-world" image from the Docker Hub
              -- Docker daemon creates a new container from that image which runs the executable that produces the output.
              -- Docker daemon streams the output to the Docker client which sends it to the terminal.
