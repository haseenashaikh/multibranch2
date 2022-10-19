pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                sh'''
                pwd
                rm -rf *
                git clone https://github.com/haseenashaikh/multibranch2.git
                '''
            }
        }
        stage('maven1'){
            steps{
                sh'''
                cd multibranch2
                mvn clean
                '''
            }
        }
        stage('maven2'){
            steps{
                sh'''
                cd multibranch2
                mvn test
                '''
            }
        }
        stage('maven3'){
            steps{
                sh'''
                cd multibranch2
                mvn clean
                '''
            }
        }
        stage('maven4'){
            steps{
                sh'''
                cd multibranch2
                mvn install package
                '''
            }
        }
    }
}
