pipeline {
    agent { label 'slave1' }
    stages {
        stage('checkout') {
            steps {
           sh 'rm -rf hello-world-war'
           sh 'git clone https://github.com/parulokesh/hello-world-war/'
            }
         }
        stage('build') {
            steps {
                sh 'mvn --version'
                sh 'mvn clean install'
                         }
        }
        stage('deploy') {
            steps {
                sh 'ssh root@172.31.9.223'
                sh ' scp /home/slave1/workspace/samplepipeline1/target/hello-world-war-1.0.0.war root@172.31.9.223:/opt/apache-tomcat-8.5.98/webapps/'
    }
}
    }
}
