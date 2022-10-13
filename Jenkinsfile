pipeline{
    agent(any)
    stages{
        stage("Build Artifact"){
            steps{
              sh "mvn  compile"
              archiveArtifacts 'target/*.jar' //so that they can be downloaded later
            }
        }

    }
}
