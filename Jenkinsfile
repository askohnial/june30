pipeline {
    agent 
    {
        node {
            label 'jenkins2-docker-slave1'
        } //closing node
      } // closing agent

    stages {
        stage('StopRemove') {
            steps {
                echo 'Removing..'
                }// closing steps 
            }// closing stage
            /*steps {
                sh 'ls -l'
                sh 'docker container stop jenkins2'
                sh 'docker container rm jenkins2'
                sh 'docker image rmi akhil5001/docker-jenkins2:latest'
           } */
        
        stage('Build') {
             /*steps {
                echo 'Building..'
                }
            
            }*/ 
            steps {
                sh 'docker build -t  akhil5001/devops_docker_2 .'
                sh 'docker container run -d --name jenkins2 -p 80:80 akhil5001/docker-jenkins2:latest'
                
            } // steps closing 
        } // closing stage
        
        stage('Push') {
            /*steps {
                echo 'Pushing..'
                }
            when {
                branch 'finance'  //only run these steps on the development branch
            }*/
            
            steps {
                sh 'docker push akhil5001/docker-jenkins2:latest'
                
            } //closing steps
            } // closing stage
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                }
            
            /*steps {
                sh 'docker container run -d --name jenkins2 -p 80:80 akhil5001/docker-jenkins2:latest'
                
           } */
           }// closing stage
    } //closing stages
} // closing pipeline
