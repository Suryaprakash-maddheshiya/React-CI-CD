pipeline {
    agent any
    stages {
        stage('Build') {
            agent{
                docker{
                    image 'node:22.11.0-alpine3.20'
                    args '-u root'
                    reuseNode true // reuse the node for the next stages

            }
            }
            step{
                 sh '''
                 ls -l
                 node --Version
                 npm --Version
                 npm install 
                 npm run build 
                 ls -l 

                 '''
                }

            steps {  
                echo 'Hello World'
            }
        }
    }
}
