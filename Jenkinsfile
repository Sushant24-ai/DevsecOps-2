pipeline{
    agent(any)
    stages{
        stage("Build Artifact-1"){
            steps{
                sh "mvn clean package -DskipTest=true"
                archive "target/*.jar"
            }
        }

    }
}
