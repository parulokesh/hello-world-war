pipeline {
    agent { label 'slave3' }
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
                sh 'ssh root@13.127.143.117'
                sh '/home/slave3/workspace/samplepipeline1/target/hello-world-war-1.0.0.war root@13.127.143.117:/opt/apache-tomcat-8.5.97/webapps'
    }
}
    }
}
