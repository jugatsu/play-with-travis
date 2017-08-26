#### Log to Travis CI

```bash
ak@ak-pc:~/Dropbox/otus/04-lesson-chatops/play-with-travis$ travis login
We need your GitHub login to identify you.
This information will not be sent to Travis CI, only to api.github.com.
The password will not be displayed.

Try running with --github-token or --auto if you don't want to enter your password anyway.

Username: jugatsu
Password for jugatsu: ********
Two-factor authentication code for jugatsu: ******
Successfully logged in as jugatsu!
```

#### Show build history
```bash
ak@ak-pc:~/Dropbox/otus/04-lesson-chatops/play-with-travis$ travis history
#9 passed:       master Merge pull request #6 from jugatsu/add-build-status
#8 passed:       master (PR #6) Add Travis CI build status to README.md
#7 passed:       add-build-status Add Travis CI build status to README.md
#6 passed:       master Merge pull request #5 from jugatsu/fix-test
#5 passed:       master (PR #5) Fix test_equel unit test
#4 passed:       fix-test Fix test_equel unit test
#3 failed:       master Merge pull request #4 from jugatsu/travis-slack
#2 failed:       master (PR #4) Add slack notification with secret token to .travis.yml
#1 failed:       travis-slack Add slack notification with secret token to .travis.yml
```

#### Show info about build job #9
```bash
ak@ak-pc:~/Dropbox/otus/04-lesson-chatops/play-with-travis$ travis show 9
Build #9:  Merge pull request #6 from jugatsu/add-build-status
State:         passed
Type:          push
Branch:        master
Compare URL:   https://github.com/jugatsu/play-with-travis/compare/e7a0c8fdc5a9...afad86703430
Duration:      1 min 13 sec
Started:       2017-08-26 14:19:56
Finished:      2017-08-26 14:20:49

#9.1 passed:     46 sec         python: 3.4, os: linux
#9.2 passed:     27 sec         python: 3.5, os: linux
```

#### Show logs of build job #9
```bash
ak@ak-pc:~/Dropbox/otus/04-lesson-chatops/play-with-travis$ travis logs 9
displaying logs for jugatsu/play-with-travis#9.1
Worker information
hostname: i-067858b-production-2-worker-org-ec2.travisci.net:805cdd1c-8e26-4b2c-bdd3-7b10e31890b6
version: v2.9.3 https://github.com/travis-ci/worker/tree/a41c772c638071fbbdbc106f31a664c0532e0c36
instance: 4b4c42f:travis:python (via amqp)
startup: 719.369495ms
....
```
