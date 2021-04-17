pipeline{
    agent none
    stages{
        stage('Gitscm'){
            agent {
                label 'mydockerarth'
            }
            steps{
                echo "This is the master  branch"      
            }
        }
    }
}
