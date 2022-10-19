pipeline{
    agent(any)
    stages{
        stage("Build Artifact"){
            steps{
              sh "mvn clean package -DskipTests=true"
              archiveArtifacts 'target/*.jar' //so that they can be downloaded later
            }
        }

        stage("Jacoco test"){
            steps{
              sh "mvn test"
            }
        }

        stage('Mutation Tests - PIT') {
             steps {
                sh "mvn org.pitest:pitest-maven:mutationCoverage"
            }
        }

         stage("SonarQube - SAST") {
             steps {
              // withSonarQubeEnv('SonarQube') {
                   sh "mvn clean verify sonar:sonar -Dsonar.projectKey=sush24 -Dsonar.host.url=http://3.237.182.74:9000/ -Dsonar.login=sqp_8f8198f5e43ac185aaab0e48283ce2757b53d924"
            }
          //   timeout(time: 2, unit: 'MINUTES') {
          //        script {
          //          waitForQualityGate abortPipeline: false
          //      }
          //  }
        // }
        }

    }
}
