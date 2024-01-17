pipeline {
    agent { lebel 'slave3' }
    stages {
        stage('checkout') {
            steps {
           sh 'rm -rf hello-world-war'
           sh 'git clone https://github.com/parulokesh/hello-world-war/'
            }
        }
        stages {
        stage('build') {
            steps {
           sh 'mvn --version'
           sh 'mvn clean install'
            }
        }
    }
}
