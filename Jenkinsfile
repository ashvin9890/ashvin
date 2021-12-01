pipeline {
  agent any
  stages {
    stage('Git Clone') {
      steps {
        git credentialsId: 'GIT', url: 'git@github.com:ashvin9890/springboot-with-docker.git'
      }
    }
          stage('build') {
      steps {
        echo "$user"
      }
    }
          stage('build_ls') {
      steps {
        echo "$pwd"
      }
    }
 
    stage('Git Clone65') {
      steps {
         sh '''
            #!/bin/bash
scp /home/ubuntu/ashvin/ashvin.yaml root@akubernetes.paysquare.com:/home/ubuntu/ashvin

'''
    }
    }
        stage('Git Clone1') {
        steps {
    sh """ssh -tt root@akubernetes.paysquare.com << EOF 
    kubectl get pod
    kubectl apply -f /home/ubuntu/ashvin/ashvin.yaml 
    exit
    EOF"""
    }
    }
            stage('Git Clone2') {
        steps {
    sh """ssh -tt root@akubernetes.paysquare.com << EOF 
    kubectl get pod
    kubectl delete -f /home/ubuntu/ashvin/ashvin.yaml 
    exit
    EOF"""
    }
    }
        }
}

