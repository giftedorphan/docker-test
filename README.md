# docker-test / Ubuntu Linux

#####  Cloning the repository
```sh
git clone https://github.com/giftedorphan/docker-test.git
```

#####  Change to your new directory
```sh
cd docker-test/
```

#####  Create a machine.
```sh
docker-machine create --driver virtualbox default
```

#####  List available machines again to see your newly minted machine.
```sh
docker-machine ls
```
[![docker-machine.jpg](https://s15.postimg.org/3umdu9yln/docker_machine.jpg)](https://postimg.org/image/rllrcdysn/)

#####  Get the environment commands for your new VM
```sh
docker-machine env
```
[![docker-machine-env.jpg](https://s4.postimg.org/g2r659qkt/docker_machine_env.jpg)](https://postimg.org/image/d8o0rtoeh/)

#####  Run this command to configure your shell:
```sh
eval $(docker-machine env)
```

#####  Build your services:
```sh
docker-compose build
```

#####  run your containers in the background:
```sh
docker-compose run  -d
```
[![docker-test-hello-app-run-background.jpg](https://s17.postimg.org/v0tre2s8v/docker_test_hello_app_run_background.jpg)](https://postimg.org/image/wfvc2stbv/)

#####  Check your containers:
```sh
docker ps
```
[![docker-test-hello-app-containers.jpg](https://s18.postimg.org/df16zo4q1/docker_test_hello_app_containers.jpg)](https://postimg.org/image/jfyvwqrc5/)

#### Check the app is running:

###### Open your web browser and type the vm ip address, you should see something like this:

[![docker-test-hello-app.jpg](https://s22.postimg.org/4m7qhd2ld/docker_test_hello_app.jpg)](https://postimg.org/image/uhrh0k4f1/)

###### Type curl (vm ip address)

[![curl-docker-test-hello-app.jpg](https://s22.postimg.org/4yiyidugx/curl_docker_test_hello_app.jpg)](https://postimg.org/image/8i4w86x6l/)

###### Should return:

[![curl-docker-test-hello-app-response.jpg](https://s18.postimg.org/7o2793yxl/curl_docker_test_hello_app_response.jpg)](https://postimg.org/image/ucre8ogb9/)

###### Also check the logs

[![docker-test-hello-app-run.jpg](https://s13.postimg.org/w1k2vl83r/docker_test_hello_app_run.jpg)](https://postimg.org/image/shy55s5dv/)
