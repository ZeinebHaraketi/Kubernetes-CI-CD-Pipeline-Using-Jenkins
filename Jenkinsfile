pipeline {
      agent any
  stages {

        stage('Cleaning up Workspace') {
            steps {
               cleanWs()
            }
        }
        
        stage('Cloning Git') {
            steps {
                git branch: 'main', url: 'https://github.com/ZeinebHaraketi/Kubernetes-CI-CD-Pipeline-Using-Jenkins.git'
            }
        }

         stage('Build App') {
            steps {
                sh 'mvn clean package'
            }
        }

         stage('Test App') {
            steps {
                sh 'mvn test '
            }
        }

        

        
}
}
