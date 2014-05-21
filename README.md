jenkins-python-template
=======================

Python-template for use in your Continuous Integration Server (jenkins).

This was inspirated by [PHP jenkins template project](http://jenkins-php.org/) ([github](https://github.com/sebastianbergmann/php-jenkins-template))

## Server requirements
```shell
# apt-get install python-dev python-virtualenv libffi-dev sloccount
```

All other programs will be installed within virtualenv.

## Jenkins Configuration

### Plugins
* [SLOCCount](http://wiki.jenkins-ci.org/display/JENKINS/SLOCCount+Plugin)
* [xUnit](http://wiki.jenkins-ci.org/display/JENKINS/xUnit+Plugin)
* [Violations](http://wiki.jenkins-ci.org/display/JENKINS/Violations)
* [Warnings](https://wiki.jenkins-ci.org/display/JENKINS/Warnings+Plugin)
* [Cobertura](https://wiki.jenkins-ci.org/display/JENKINS/Cobertura+Plugin)
* [Disk Usage](https://wiki.jenkins-ci.org/display/JENKINS/Disk+Usage+Plugin)
* [Git](https://wiki.jenkins-ci.org/display/JENKINS/Git+Plugin)

### Install Plugins

Download jenkins-cli
```shell
wget http://jenkins-server:8080/jnlpJars/jenkins-cli.jar
```

Then, install it!
```shell
java -jar jenkins-cli.jar -s http://jenkins-server:8080 install-plugin  sloccount xunit violations warnings cobertura disk-usage git
java -jar jenkins-cli.jar -s http://jenkins-server:8080 safe-restart
```

Create a new Job.
