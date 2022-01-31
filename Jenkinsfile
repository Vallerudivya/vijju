pipeline {
    agent any

    stages {
        stage('contineous download') {
            steps {
               git 'https://github.com/Vallerudivya/DemoATC.git'
            }
        }
         stage('contineous build') {
            steps {
               sh 'mvn install'
            }
        }
         stage('contineous deployment') {
            steps {
             sh 'sshpass -p "divya" scp target/DemoATR.war root@172.17.0.3:/var/lib/apache-tomcat-9.0.56/webapps'
            }
        }
    }
}

