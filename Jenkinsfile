pipeline {
    agent any
    environment {
        PATH = "/opt/maven3.9.6/bin:$PATH"
    }
    stages {
        stage("Pull Code") {
            steps {
               git branch: "master", url: "https://github.com/adikesavanaidug2404/mavenproject.git"
            }
        }
        stage("Maven Build") {
            steps {
                sh "mvn clean install"
            }
        }
     }
 }
