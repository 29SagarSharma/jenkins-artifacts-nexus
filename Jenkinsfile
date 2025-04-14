pipeline {
    agent any
    tools {
        maven "jenkins-maven"
    }
   
    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/RAHAMSHAIK007/jenkins-java-project.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('artifact') {
            steps {
                sh 'mvn package'
            }
        }
        stage('upload artifacts') {
    steps {
        script {
            nexusArtifactUploader(
                nexusVersion: 'nexus3',
                protocol: 'http',
                nexusUrl: '3.111.213.159:8081',
                groupId: 'in.RAHAM',
                version: '1.2.2',
                repository: 'WebApp',
                credentialsId: 'nexus-credentials',
                artifacts: [
                    [
                        artifactId: 'NETFLIX',
                        classifier: '',
                        file: 'target/NETFLIX-1.2.2.war',
                        type: 'war'
                    ]
                ]
            )
        }
    }
}

        
        
    }    
    
}