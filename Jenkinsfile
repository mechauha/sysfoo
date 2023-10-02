pipeline {
    agent any
    tools{
      maven 'Maven 3.6.3'
    }

    stages {
        stage('Build') {
            steps {
                echo 'building sysfoo app'
                sh 'mvn complile'
            }
        }
        stage('test') {
            steps {
                echo 'running unit test'
                sh 'mvn clean test'
            }
        }
        stage('package') {
            steps {
                echo 'generating .war file'
                sh 'mvn package -DskipTests'
            }
        }
    }
    post{
        always{
            echo 'This pipeline is completed !!'
        }
    }
}
