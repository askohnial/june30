pipeline {
    agent any
    /*{
        node {
            label 'devops_docker_2'
        }
      } */

    stages {
        stage('StopRemove') {
            steps {
                echo 'Removing..'
                }
            }
            /*steps {
                sh 'ls -l'
                sh 'docker container stop dptwo'
                sh 'docker container rm dptwo'
                sh 'docker image rmi akhil5001/devops_docker_2:latest'
           } */
        
        stage('Build') {
            steps {
                echo 'Building..'
                }
            
            }
            /*steps {
                sh 'docker build -t  akhil5001/devops_docker_2 .'
                // sh 'docker container run -d --name dptwo -p 80:80 akhil5001/devops_docker_2:latest'
                
            }*/
        
        stage('Push') {
            steps {
                echo 'Pushing..'
                }
            /*when {
                branch 'finance'  //only run these steps on the development branch
            }
            
            steps {
                sh 'docker push akhil5001/devops_docker_2:latest'
                
            }*/
            }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                }
            
            /*steps {
                sh 'docker container run -d --name dptwo -p 80:80 akhil5001/devops_docker_2:latest'
                
           } */
           }
    }
}
