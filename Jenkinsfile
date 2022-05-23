pipeline {
    agent any
    
    stages {
        stage ('git') {
            steps {
            git 'https://github.com/chandrikakmc1997/mavenproject-using-pipeline.git'
        }
        }
        stage ('build') {
            steps {
                bat "mvn clean package"
            }
        }
    }
}
