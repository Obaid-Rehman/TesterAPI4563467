node {
    stage('Checkout') {
        checkout scm
    }
    stage('Prepare') {
        if (isUnix()) {
            sh "dotnet restore"
        } else {
            bat "dotnet restore"
        }
    }
    stage('Build') {
        if (isUnix()) {
            sh "dotnet build -c Release"
        } else {
            bat "dotnet build -c Release"
        }
    }
    stage('Test') {
        if (isUnix()) {
            sh "dotnet test -v detailed -c Release"
        } else {
            bat "dotnet test -v detailed -c Release"
        }
    }
}