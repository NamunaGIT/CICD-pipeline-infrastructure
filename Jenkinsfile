pipeline{
    agent any
    tools {
  terraform 'terraform'
}
stages{
    stage('Git check out'){
        steps{
            git branch: 'main', url: 'https://github.com/NamunaGIT/CICD-pipeline-infrastructure.git'
        }
    }
        stage('terraform init'){
        steps{
            sh 'terraform init'
        }
    }
            stage('terraform apply'){
        steps{
            sh 'terraform apply --auto-approve'
        }
    }
}
}
