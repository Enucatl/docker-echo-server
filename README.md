# Docker Echo Server

Simple docker container which just echo data sent on UDP and TCP port.

Can be useful when doing some network tests.

Available on Docker Hub as `vhiribarren/echo-server`

Run memo:

    $ docker compose build
    $ docker compose run --rm -it --service-ports echo-server

Test memo:

    $ nc -u localhost 4001 # may be necessary to force IPv4 on MacOS
    $ nc localhost 5001
