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
     }
}