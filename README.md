## Deploy and start with VM

1. run your VM 
2. copy public IP of VM 
* for example, `84.201.161.27`
3. enter to VM 
* `ssh 84.201.161.27 -A -l admin`
4. install docker 
* `sudo apt-get install docker.io`
5. add user admin to group docker 
* `sudo gpasswd -a admin docker`
* `logout`
* `ssh 84.201.161.27 -A -l admin`
6. clone project 
* `git clone git@github.com:nimestel/flatris.git`
7. go to project dir
* `cd flatris`
8. build project 
* `docker-compose build`
* or `docker build . -t flatris`
9. run project
* `docker-compose up`
* or `docker run -it -p 3000:3000 flatris`
10. enjoy app on public IP address of VM with 3000 port
* `http://84.201.161.27:3000/`


[![Flatris](flatris.png)](https://flatris.space/)

[![Build Status](https://travis-ci.org/skidding/flatris.svg?branch=master)](https://travis-ci.org/skidding/flatris)

> **Work in progress:** Flatris has been recently redesigned from the ground up and turned into a multiplayer game with both UI and server components. This has been an interesting journey and I plan to document the architecture in depth. **[Stay tuned](https://twitter.com/skidding)**.

[![Flatris](flatris.gif)](https://flatris.space/)

> **Contribution disclaimer:** Flatris is a web game with an opinionated feature set and architectural design. It doesn't have a roadmap. While I'm generally open to ideas, I would advise against submitting unannounced PRs with new or modified functionality. That said, **bug reports and fixes are most appreciated.**

Thanks [@paulgergely](https://twitter.com/paulgergely) for the initial flat design!

Also see [elm-flatris](https://github.com/w0rm/elm-flatris).


## Setup and running

```
yarn install
yarn test
yarn build
yarn start
```

Go to http://localhost:3000
