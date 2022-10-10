pipeline{
    agent(any)
    stages{
        stage("Build Artifact"){
            steps{
                sh "mvn clean package -DskipTest=true"
                archive "target/*.jar"
            }
        }

    }
}
