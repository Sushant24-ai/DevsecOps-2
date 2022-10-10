pipeline{
    agent(any)
    stages{
        stage("Build Artifact-1"){
            steps{
                sh "docker build -t sush24 ."
                /*archive "target/*.jar"*/
            }
        }

    }
}
