pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    bat "sh ./gradlew compileJava"
               }
          }
          stage("Unit test") {
               steps {
                   bat "sh ./gradlew test"
               }
          }
          stage("Code coverage") {
            steps {
                bat "sh ./gradlew jacocoTestReport"
                publishHTML (target: [
                               reportDir: 'build/reports/jacoco/test/html',
                               reportFiles: 'index.html',
                               reportName: "JaCoCo Report"
                          ])
                bat "sh ./gradlew jacocoTestCoverageVerification"
            }
          }
     }
}