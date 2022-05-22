node {
  stage ('Build') {
    git url: 'https://github.com/chandrikakmc1997/mavenproject-using-pipeline.git'
    withMaven {
      sh "mvn clean verify"
    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe reports and FindBugs reports
  }
}
