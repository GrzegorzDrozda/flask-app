pipeline {
    agent any
    stages {
        stage('Deploy to Saging') {
            steps {
                echo 'Deploying to staging'
                ansiblePlaybook(credentialsId: 'jenkins1', inventory: 'ansible/inventory/hosts', playbook: 'ansible/playbooks/implement.yml')
                //sh './gradlew build --no-daemon'
                //#rchiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to production'
                //sh './gradlew build --no-daemon'
                //archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }

    }
}
