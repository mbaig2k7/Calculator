pipeline {
    agent any
    stages {
        stage("clone code") {
            steps {
                script {
                    // Let's clone the source
                    git 'https://github.com/mbaig2k7/Calculator.git';
                }
            }
        }
         stage("mvn build") {
            steps {
                    sh 'mvn -X clean package'
                }
        }
         stage("docker build") {
            steps {
                    sh 'docker build .'
                }
        }
         stage("deploy") {
            steps {
                    sh 'docker run -it imagename'
                }
        }
}
}
