#!groovy

stage 'Dev'
node ('master') {
    checkout scm
    mvn 'clean package'
    dir('target') {stash name: 'war', includes: 'x.war'}
}

def mvn(args) {
    bat "${tool 'Maven 3.x'}/bin/mvn ${args}"
}