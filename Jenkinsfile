pipeline {
    agent any

    stages {
        stage('Compile Stage'){

            steps{
                withMaven(maven: 'maven_3_8_4'){
                    bat 'mvn clean compile'
                }
                echo 'Compile App'
            }
        }

        stage('Testing Stage'){

            steps{
                withMaven(maven: 'maven_3_8_4'){
                    bat 'mvn test'
                }
                echo 'Test App'
            }
        }

        stage('Deployment Stage'){
            steps{
                withMaven(maven: 'maven_3_8_4'){
                    bat 'mvn deploy'
                }
                echo 'Deploy App'
            }
        }
    }
}