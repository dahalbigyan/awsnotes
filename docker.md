1. Get Docker Community Edition(CE) for Mac
    - Install Docker.dmg
    - Includes:
        a) Docker Engine
        b) Docker CLI client
        c) Docker Compose
        d) Docker Machine
        e) Kitematic
2. Start Docker
    - docker version
    - docker run hello-world
        -- Docker client contacts Docker daemon
              -- Docker daemon pulls the "hello-world" image from the Docker Hub
              -- Docker daemon creates a new container from that image which runs the executable that produces the output.
              -- Docker daemon streams the output to the Docker client which sends it to the terminal.
    - docker run -it ubuntu bash
    - docker run -d -p 80:80 --name webserver nginx
    - host_port: container_port
3.View the details on the container
  - docker container ls || docker ps

4. Docker Networking Options
    - Default Docker Bridge
          - Ethernet Cable
          - IP Table
          - Default Docker Bridge/Docker 0
          - Container1, Container2
          - NAT outbound/inbound
    - Great Resources
    https://www.oreilly.com/learning/what-is-docker-networking
    https://www.youtube.com/watch?v=Xxhhdo2e-DA

*****
Regardless of single-host deployment || muti-host deployments, you will always have to deal with networking.
a) Single Host Deployments:
    - The question boils down to data exchange via:
    i) shared volume(faster speed)
    ii) networking(HTTP based or otherwise)
b) Multi-host deployments:
    - How are containers communicating within a host?
    - How does the communication paths look between different hosts?
****
Docker Networking
1. Bridge Mode
      - Docker daemon creates docker0
      - eth0 interface
      - Default bridges vs. User defined bridges vs. Overlay Network
2. Host Mode
3. Container Mode
4. No Networking Mode


**** docker info ***
{
  Containers: 0,
  Running: 0,
  Paused: 0,
  Stopped: 0,
  Images: 0,
  Server Version: 18.03.1,
  Storage Driver: overlay2,
  Backing Filesystem: extfs,
  Supports d_type: true,
  Native Overlay Diff: true,
  Logging Driver: cgroupfs,
  Pluggins: {
    Volume: local,
    Network: 'bridge host ipvlan macvlan null overlay2'
    Log: 'awslogs fluentd gcplogs gelf journald json-file logentries splunk syslog'
  },
  Swarm: inactive ,
  Runtimes: runc,
  Default Runtime: runc,
  Init Binary: docker-nit,
  containerd version: '',
  ....etc
}
