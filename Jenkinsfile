pipeline {
     agent {
           label 'master'
       }
     stages {
         
         stage('Pull') {
              steps {
                 echo "Build stage is running"
                 git branch: 'main', url: 'https://github.com/RohitKakde27/kubernetes-deployment.git'
                    }
                        }
         
         
         stage("Docker build"){
              sshagent(['docker'])  {
        sh 'sudo chown centos:centos  /var/run/docker.sock '
        sh 'docker version'
        sh 'docker build -t jhooq-docker-demo .'
        sh 'docker image list'
        sh 'docker tag jhooq-docker-demo rahulwagh17/jhooq-docker-demo:jhooq-docker-demo'
                     }      
                             }
         
         
         stage('Test') {
              steps {
                 echo "Build stage is running"
                    }
                        }
         
         
         stage('Deploy') {
              steps {
                 echo "Build stage is running"
                    }
                         }
            }
}


