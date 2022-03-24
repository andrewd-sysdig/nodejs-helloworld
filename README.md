# nodejs-helloworld
Simple NodeJS Helloworld app that has a vulnerability we can fix as part of a demo

## Steps
* Kick off a pipeline build and show result in new scanning engine by filtering for Vulnerabilities that have a fix and you should see CVE-2002-0078 and CVE-2021-4160 which are both caused by libessl1.1 version 1.1.1k-1+deb11u1
* Update the Dockerfile to update this package by uncommenting line 9: RUN apt update && apt upgrade libssl1.1 -y
* Wait for new build to finish and post results to new scanning engine in the Sysdig UI and show that there are now no Fixable Vulnerabilities in this image
