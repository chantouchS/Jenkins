pipeline {
    agent any 
    stage('Build') {
            steps {
                sh 'echo "Build : Python - nothing to do"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Test : not implemented"'
            }
        }
        stage('Deploy') {
            steps {
                // withCredentials([azureServicePrincipal('AzureServicePrincipalID')]) {
                //     sh 'az login --service-principal -u $AZURE_CLIENT_ID -p $AZURE_CLIENT_SECRET -t $AZURE_TENANT_ID'
                //     sh 'az account set -s $AZURE_SUBSCRIPTION_ID'
                //     sh 'pwd'
                //     sh 'export'
                //     sh 'chmod +x ./deploy/az-webapp-create-py.sh'
                //     sh './deploy/az-webapp-create-py.sh -z . -b $BUILD_TAG'
                // }
                sh 'pwd'
                sh 'export'
                sh 'chmod +x ./deployment/az-webapp-create-py.sh'
                sh './deployment/az-webapp-create-py.sh'
            }
        }
    }
}