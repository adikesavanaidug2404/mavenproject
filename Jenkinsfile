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
        stage("QA-Deploy") {
            steps {
                sshagent(['adikesava']) {sh "scp -oStrictHostKeyChecking=no /var/lib/jenkins/workspace/deploy/webapp/target/webapp.war root@10.0.8.142:/opt/apache-tomcat-10.1.17/webapps"
                    
     }
 }
