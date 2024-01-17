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
                sh 'mvn clean intall'
                         }
        }
    }
}
