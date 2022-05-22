pipeline {
    agent any

   // tools {
        // Install the Maven version configured as "M3" and add it to the path.
     //   maven "C:/Program Files/apache-maven-3.8.5/bin"
    //}

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/chandrikakmc1997/mavenproject-using-pipeline.git'
                sh "mvn clean install"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts 'target/*.jar'
                }
            }
        }
    }
}
