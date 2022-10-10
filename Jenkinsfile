pipeline{
    agent(any)
    stages{
        stage("Build Artifact-1"){
            steps{
                sh "docker build sush24 ."
                /*archive "target/*.jar"*/
            }
        }

    }
}
