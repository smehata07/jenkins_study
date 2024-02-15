pipeline {
    agent any

    stages {
        stage('Terraform Init') {
            steps {
                script {
                    // Define the Terraform executable path
                    def terraformHome = tool name: 'Terraform-1.7.3-windows', type: 'terraform'
                    def terraformExe = "${terraformHome}\\terraform.exe"
                    
                    // Check Terraform version
                    def versionStatus = bat script: "${terraformExe} --version", returnStatus: true
                    if (versionStatus == null) {
                        error 'Failed to retrieve Terraform version'
                    } else {
                        echo "The Terraform version is :${versionStatus}"
                        echo "Current working directory: ${pwd()}"
                    }
                }
            }
        }
    }
}
