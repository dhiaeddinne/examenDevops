pipeline {


    agent any


    stages {

        stage("Cloning Project"){
            steps {
                git branch: 'main',
                url: 'https://github.com/dhiaeddinne/examenDevops.git'
                echo 'checkout stage'
            }
        }

        stage ('Maven Clean'){
            steps
			{
                sh 'mvn clean'
            }
        }

		stage ('Maven Compile'){
            steps
			{
                sh 'mvn compile'
            }
        }

        stage ('Maven Test'){
            steps
			{
                sh 'mvn test'
            }
        }

		stage('Maven Build'){
            steps
			{
                sh 'mvn package'
            }
        }

		stage ('Maven Install'){
            steps
			{
                sh 'mvn install'
            }
        }

    //         stage('MVN SONARQUBE') {
    //   steps {
    //     sh 'docker run -d --name sonarqube -p 9000:9000 sonarqube'
    //     sh 'docker run -e SONAR_HOST_URL=http://192.168.1.5/:9000 -v $(pwd):/usr/src sonarsource/sonar-scanner'
    //   }
    // }

    //     stage('Test') {
    //         steps {
    //             sh 'docker run myapp mvn test'
    //         }
    //         post {
    //             always {
    //             junit 'target/surefire-reports/*.xml'
    //             }
    //         }
    // }
    }
}
