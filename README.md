# CI-CD
# my console ouptput upon running my first multiagent docker slave CI/CD pipeline
Started by user leelakrishna
Obtained multi-stage-multi-agent/Jenkinsfile from git https://github.com/Memory123456789/Jenkins-Zero-To-Hero/
[Pipeline] Start of Pipeline
[Pipeline] stage
[Pipeline] { (Back-end)
[Pipeline] node
Running on Jenkins in /var/lib/jenkins/workspace/jenkins-pipeline
[Pipeline] {
[Pipeline] checkout
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/jenkins-pipeline/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/Memory123456789/Jenkins-Zero-To-Hero/ # timeout=10
Fetching upstream changes from https://github.com/Memory123456789/Jenkins-Zero-To-Hero/
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/Memory123456789/Jenkins-Zero-To-Hero/ +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse origin/main^{commit} # timeout=10
Checking out Revision 3f239ea1e926abfdc403798c25c4801ff797b7b8 (origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 3f239ea1e926abfdc403798c25c4801ff797b7b8 # timeout=10
Commit message: "Clarified Docker permission steps for Jenkins and Ubuntu users"
 > git rev-list --no-walk 3f239ea1e926abfdc403798c25c4801ff797b7b8 # timeout=10
[Pipeline] withEnv
[Pipeline] {
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker inspect -f . maven:3.8.1-adoptopenjdk-11
.
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] withDockerContainer
Jenkins does not seem to be running inside a container
$ docker run -t -d -u 111:113 -w /var/lib/jenkins/workspace/jenkins-pipeline -v /var/lib/jenkins/workspace/jenkins-pipeline:/var/lib/jenkins/workspace/jenkins-pipeline:rw,z -v /var/lib/jenkins/workspace/jenkins-pipeline@tmp:/var/lib/jenkins/workspace/jenkins-pipeline@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** maven:3.8.1-adoptopenjdk-11 cat
$ docker top d74cf41db39ef6083e2be733f9202c3aaf755698c747eecb83d8939c982123c3 -eo pid,comm
[Pipeline] {
[Pipeline] sh
+ mvn --version
Apache Maven 3.8.1 (05c21c65bdfed0f71a2f2ada8b84da59348c4c5d)
Maven home: /usr/share/maven
Java version: 11.0.11, vendor: AdoptOpenJDK, runtime: /opt/java/openjdk
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "6.8.0-1029-aws", arch: "amd64", family: "unix"
[Pipeline] }
$ docker stop --time=1 d74cf41db39ef6083e2be733f9202c3aaf755698c747eecb83d8939c982123c3
$ docker rm -f --volumes d74cf41db39ef6083e2be733f9202c3aaf755698c747eecb83d8939c982123c3
[Pipeline] // withDockerContainer
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Front-end)
[Pipeline] node
Running on Jenkins in /var/lib/jenkins/workspace/jenkins-pipeline
[Pipeline] {
[Pipeline] checkout
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/jenkins-pipeline/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/Memory123456789/Jenkins-Zero-To-Hero/ # timeout=10
Fetching upstream changes from https://github.com/Memory123456789/Jenkins-Zero-To-Hero/
 > git --version # timeout=10
 > git --version # 'git version 2.43.0'
 > git fetch --tags --force --progress -- https://github.com/Memory123456789/Jenkins-Zero-To-Hero/ +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse origin/main^{commit} # timeout=10
Checking out Revision 3f239ea1e926abfdc403798c25c4801ff797b7b8 (origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 3f239ea1e926abfdc403798c25c4801ff797b7b8 # timeout=10
Commit message: "Clarified Docker permission steps for Jenkins and Ubuntu users"
[Pipeline] withEnv
[Pipeline] {
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker inspect -f . node:16-alpine
.
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] withDockerContainer
Jenkins does not seem to be running inside a container
$ docker run -t -d -u 111:113 -w /var/lib/jenkins/workspace/jenkins-pipeline -v /var/lib/jenkins/workspace/jenkins-pipeline:/var/lib/jenkins/workspace/jenkins-pipeline:rw,z -v /var/lib/jenkins/workspace/jenkins-pipeline@tmp:/var/lib/jenkins/workspace/jenkins-pipeline@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** node:16-alpine cat
$ docker top 9acca66951f0c520ede98720d7755f1db30665288f6ba294e0e0621d057bf417 -eo pid,comm
[Pipeline] {
[Pipeline] sh
+ node --version
v16.20.2
[Pipeline] }
$ docker stop --time=1 9acca66951f0c520ede98720d7755f1db30665288f6ba294e0e0621d057bf417
$ docker rm -f --volumes 9acca66951f0c520ede98720d7755f1db30665288f6ba294e0e0621d057bf417
[Pipeline] // withDockerContainer
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] }
[Pipeline] // stage
[Pipeline] End of Pipeline
Finished: SUCCESS
