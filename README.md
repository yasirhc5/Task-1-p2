# assignment-1-part-2

# Step-1 Using the docker image from Part 1

Already build in part-1 image will be used that is myapp.

# Step-2 Run the Docker Container

# Command To Exec
docker run -p 3000:3000 myapp

# Output
> yasirhc5.0.0 start /app
> node app.js

Server running at http://0.0.0.0:3000/

3000 is the port we exposed in part 1 and myapp is the image name from part 1

# Step-3 Use Different Docker Container Commands
For this i will need to use another terminal window so that container keep running in the existing one.

■ 'docker ps' command to list all running containers
# Command To Exec
docker ps

# Output
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                                       NAMES
7d832e88d3ca   myapp     "docker-entrypoint.s…"   12 seconds ago   Up 10 seconds   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   hungry_nightingale

■ 'docker stop' command to stop a running container

■ 'docker rm' command to remove a stopped container

■ 'docker logs' command to view the logs of a container
# Command To Exec
docker logs 7d832e88d3ca 

# Output
> yasirhc5.0.0 start /app
> node app.js

Server running at http://0.0.0.0:3000/

■ 'docker inspect' command to view the details of a container
# Command To Exec
docker inspect 7d832e88d3ca

# Output
[
    {
        "Id": "7d832e88d3ca2d2b719cf7924d767bff654dd6640664d1ff5404711b0bf37fe2",
        "Created": "2023-03-31T11:18:07.280608177Z",
        "Path": "docker-entrypoint.sh",
        "Args": [
            "npm",
            "start"
        ],
        "State": {
            "Status": "running",
            "Running": true,
            "Paused": false,
            "Restarting": false,
            "OOMKilled": false,
            "Dead": false,
            "Pid": 10220,
            "ExitCode": 0,
            "Error": "",
            "StartedAt": "2023-03-31T11:18:08.849287638Z",
            "FinishedAt": "0001-01-01T00:00:00Z"
        },
        "Image": "sha256:4e466b4d01a1c472e11dd441150568d241791d11571e4a124d60c6de1f52457a",
        "ResolvConfPath": "/var/lib/docker/containers/7d832e88d3ca2d2b719cf7924d767bff654dd6640664d1ff5404711b0bf37fe2/resolv.conf",
        "HostnamePath": "/var/lib/docker/containers/7d832e88d3ca2d2b719cf7924d767bff654dd6640664d1ff5404711b0bf37fe2/hostname",
        "HostsPath": "/var/lib/docker/containers/7d832e88d3ca2d2b719cf7924d767bff654dd6640664d1ff5404711b0bf37fe2/hosts",
        "LogPath": "/var/lib/docker/containers/7d832e88d3ca2d2b719cf7924d767bff654dd6640664d1ff5404711b0bf37fe2/7d832e88d3ca2d2b719cf7924d767bff654dd6640664d1ff5404711b0bf37fe2-json.log",
        "Name": "/hungry_nightingale",
        "RestartCount": 0,
        "Driver": "overlay2",
        "Platform": "linux",
        "MountLabel": "",
        "ProcessLabel": "",
        "AppArmorProfile": "docker-default",
        "ExecIDs": null,
        "HostConfig": {
            "Binds": null,
            "ContainerIDFile": "",
            "LogConfig": {
                "Type": "json-file",
                "Config": {}
            },
            "NetworkMode": "default",
            "PortBindings": {
                "3000/tcp": [
                    {
                        "HostIp": "",
                        "HostPort": "3000"
                    }
                ]
            },
            "RestartPolicy": {
                "Name": "no",
                "MaximumRetryCount": 0
            },
            "AutoRemove": false,
            "VolumeDriver": "",
            "VolumesFrom": null,
            "ConsoleSize": [
                29,
                79
            ],
            "CapAdd": null,
            "CapDrop": null,
            "CgroupnsMode": "private",
            "Dns": [],
            "DnsOptions": [],
            "DnsSearch": [],
            "ExtraHosts": null,
            "GroupAdd": null,
            "IpcMode": "private",
            "Cgroup": "",
            "Links": null,
            "OomScoreAdj": 0,
            "PidMode": "",
            "Privileged": false,
            "PublishAllPorts": false,
            "ReadonlyRootfs": false,
            "SecurityOpt": null,
            "UTSMode": "",
            "UsernsMode": "",
            "ShmSize": 67108864,
            "Runtime": "runc",
            "Isolation": "",
            "CpuShares": 0,
            "Memory": 0,
            "NanoCpus": 0,
            "CgroupParent": "",
            "BlkioWeight": 0,
            "BlkioWeightDevice": [],
            "BlkioDeviceReadBps": [],
            "BlkioDeviceWriteBps": [],
            "BlkioDeviceReadIOps": [],
            "BlkioDeviceWriteIOps": [],
            "CpuPeriod": 0,
            "CpuQuota": 0,
            "CpuRealtimePeriod": 0,
            "CpuRealtimeRuntime": 0,
            "CpusetCpus": "",
            "CpusetMems": "",
            "Devices": [],
            "DeviceCgroupRules": null,
            "DeviceRequests": null,
            "MemoryReservation": 0,
            "MemorySwap": 0,
            "MemorySwappiness": null,
            "OomKillDisable": null,
            "PidsLimit": null,
            "Ulimits": null,
            "CpuCount": 0,
            "CpuPercent": 0,
            "IOMaximumIOps": 0,
            "IOMaximumBandwidth": 0,
            "MaskedPaths": [
                "/proc/asound",
                "/proc/acpi",
                "/proc/kcore",
                "/proc/keys",
                "/proc/latency_stats",
                "/proc/timer_list",
                "/proc/timer_stats",
                "/proc/sched_debug",
                "/proc/scsi",
                "/sys/firmware"
            ],
            "ReadonlyPaths": [
                "/proc/bus",
                "/proc/fs",
                "/proc/irq",
                "/proc/sys",
                "/proc/sysrq-trigger"
            ]
        },
        "GraphDriver": {
            "Data": {
                "LowerDir": "/var/lib/docker/overlay2/8acd17ec545c4105f4a69af299049dc90cbc963304fc35e61bbe603e6f49e677-init/diff:/var/lib/docker/overlay2/hizdlmp6hkfrke1w9z8bl3icn/diff:/var/lib/docker/overlay2/ttt9ormqcsvmhvo46miwz9fib/diff:/var/lib/docker/overlay2/n0oxlkviqz7nfj97xrf4gj4nd/diff:/var/lib/docker/overlay2/l992sst3huxp5g6ugfdawygwl/diff:/var/lib/docker/overlay2/c80923795f195c9db3a98d40d3b24871ce1de7c12a5b53cc71faa4c4a29d95dc/diff:/var/lib/docker/overlay2/99db273c7b438f69a9c636ce534aa80d43aa2d00aa4706307c60b04b8a93f2b8/diff:/var/lib/docker/overlay2/3ab5433d729c05ef97d222ff163d1951b551110d59cbf60288d69cab723dce7c/diff:/var/lib/docker/overlay2/47be2dc6dee00132e5c9cd5b35da95169e24d865e0a2036920be05a9d0d51256/diff",
                "MergedDir": "/var/lib/docker/overlay2/8acd17ec545c4105f4a69af299049dc90cbc963304fc35e61bbe603e6f49e677/merged",
                "UpperDir": "/var/lib/docker/overlay2/8acd17ec545c4105f4a69af299049dc90cbc963304fc35e61bbe603e6f49e677/diff",
                "WorkDir": "/var/lib/docker/overlay2/8acd17ec545c4105f4a69af299049dc90cbc963304fc35e61bbe603e6f49e677/work"
            },
            "Name": "overlay2"
        },
        "Mounts": [],
        "Config": {
            "Hostname": "7d832e88d3ca",
            "Domainname": "",
            "User": "",
            "AttachStdin": false,
            "AttachStdout": true,
            "AttachStderr": true,
            "ExposedPorts": {
                "3000/tcp": {}
            },
            "Tty": false,
            "OpenStdin": false,
            "StdinOnce": false,
            "Env": [
                "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
                "NODE_VERSION=14.21.3",
                "YARN_VERSION=1.22.19"
            ],
            "Cmd": [
                "npm",
                "start"
            ],
            "Image": "myapp",
            "Volumes": null,
            "WorkingDir": "/app",
            "Entrypoint": [
                "docker-entrypoint.sh"
            ],
            "OnBuild": null,
            "Labels": {}
        },
        "NetworkSettings": {
            "Bridge": "",
            "SandboxID": "898d3e40075d1344a7c5925bc6b1b9955c92eb1b06b365b2d23fb48afa6730f5",
            "HairpinMode": false,
            "LinkLocalIPv6Address": "",
            "LinkLocalIPv6PrefixLen": 0,
            "Ports": {
                "3000/tcp": [
                    {
                        "HostIp": "0.0.0.0",
                        "HostPort": "3000"
                    },
                    {
                        "HostIp": "::",
                        "HostPort": "3000"
                    }
                ]
            },
            "SandboxKey": "/var/run/docker/netns/898d3e40075d",
            "SecondaryIPAddresses": null,
            "SecondaryIPv6Addresses": null,
            "EndpointID": "f9dff734cad952bce2b4336a72bfccf04fea62f4dea8d5dbbf7f02c2194951be",
            "Gateway": "172.17.0.1",
            "GlobalIPv6Address": "",
            "GlobalIPv6PrefixLen": 0,
            "IPAddress": "172.17.0.2",
            "IPPrefixLen": 16,
            "IPv6Gateway": "",
            "MacAddress": "02:42:ac:11:00:02",
            "Networks": {
                "bridge": {
                    "IPAMConfig": null,
                    "Links": null,
                    "Aliases": null,
                    "NetworkID": "7264632a5f0df678fee795b1a0745e65241cece6121365fd1e5d8cf6d1704c5f",
                    "EndpointID": "f9dff734cad952bce2b4336a72bfccf04fea62f4dea8d5dbbf7f02c2194951be",
                    "Gateway": "172.17.0.1",
                    "IPAddress": "172.17.0.2",
                    "IPPrefixLen": 16,
                    "IPv6Gateway": "",
                    "GlobalIPv6Address": "",
                    "GlobalIPv6PrefixLen": 0,
                    "MacAddress": "02:42:ac:11:00:02",
                    "DriverOpts": null
                }
            }
        }
    }
]

■ 'docker exec' command to execute a command inside a running container
# Command To Exec
docker exec 7d832e88d3ca

# Output
app.js
package-lock.json
package.json

■ 'docker attach' command to attach to a running container
# Command To Exec
docker attach 7d832e88d3ca

# Output

■ 'docker commit' command to create a new image from a container
# Command To Exec
docker commit 7d832e88d3ca

# Output
sha256:b0ed231736a4fde748da0e0638c05a9e6b5c10647c42ece14ac7ef9f47020180
■ 'docker cp' command to copy files/folders between the container and the
host
# Command To Exec
docker cp 

# Output

■ 'docker stats' command to view the resource usage of containers
# Command To Exec
docker stats 

# Output
Stats like resource usage statistics.

■ 'docker top' command to view the running processes inside a container
# Command To Exec
docker top 5c2ac7e4cc40

Here the ID is changed bcz server was stopped and restarted

# Output
UID                 PID                 PPID                C                   STIME               TTY                 TIME                CMD
root                10844               10819               0                   16:47               ?                   00:00:01            npm
root                10886               10844               0                   16:47               ?                   00:00:00            node app.js

■ 'docker start' command to start a stopped container
# Command To Exec
docker start confident_lalande

# Output
confident_lalande

■ 'docker pause' command to pause a running container
# Command To Exec
docker pause 5c2ac7e4cc40

# Output
confident_lalande

■ 'docker unpause' command to unpause a paused container
# Command To Exec
docker unpause 5c2ac7e4cc40

# Output

■ 'docker rename' command to rename a container
# Command To Exec
docker rename confident_lalande abdul_basit

# Output
The output i got via docker ps is 
CONTAINER ID   IMAGE     COMMAND                  CREATED          STATUS          PORTS                                       NAMES
5c2ac7e4cc40   myapp     "docker-entrypoint.s…"   18 minutes ago   Up 17 minutes   0.0.0.0:3000->3000/tcp, :::3000->3000/tcp   yasir_hc5


■ 'docker wait' command to wait for a container to exit and then display its exit code
# Command To Exec
docker wait yasir_hc5

# Output

■ 'docker attach' command to attach local standard input, output, and error
streams to a running container
# Command To Exec
docker run --name 5c2ac7e4cc40 myapp

then 

docker attach 5c2ac7e4cc40

# Output

■ 'docker port' command to display the public-facing port that a container is listening on
# Command To Exec
docker port yasir_hc

# Output
3000/tcp -> 0.0.0.0:3000
3000/tcp -> [::]:3000

■ 'docker update' command to update a container's resource limits
# Command To Exec
docker update --memory 256m 5c2ac7e4cc40

# Output

■ 'docker restart' command to restart a running container
# Command To Exec
docker restart 5c2ac7e4cc40

# Output
5c2ac7e4cc40
