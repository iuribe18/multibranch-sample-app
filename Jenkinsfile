pipeline {
    agent any
    options {
        buildDiscarder logRotator (artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
        disableConcurrentBuilds()
    }
    stages {
        stage('Example') {
            steps {
                echo 'Hello World'
            }
        }
        stage('cat README.md') {
            when {
              branch "test*"
            }
            steps {
              sh '''
                cat README.md
              '''
            }
        }
    }
}