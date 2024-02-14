pipeline{
    agent any
    environment{
    var1 = 'Sonu Mehata'
    }
    stages{
        stage('Build'){
            steps{
                echo "This is a Build stage of your pipeline"
            }
        }
        stage('Test'){
            steps{
                echo "This is a Test stage of your pipeline"
            }
        }
        stage('Deploy'){
            steps{
                echo "This is a Deploy stage of your pipeline"
            }
            
        }
        stage('Environment-Test'){
                steps{
                echo "This is Environment variable: $var1"
                }
        }
    }
}
