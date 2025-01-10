pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M399"
    }

    stages {
        stage('Echo Version'){
            steps{
             sh 'echo print Maven Version'
             sh 'mvn -version'   
            }
            
        }
        stage('Build'){
            steps{
                //Get source code from repository
                //git 'https://github.com/sidd-harth/jenkins-hello-world.git'
                //Run Maven Package CMD
                sh "mvn clean package -DskipTests=True"
            }
        }
        stage('Test'){
            steps{
                sh "mvn test"
            }
        }
    }
}
