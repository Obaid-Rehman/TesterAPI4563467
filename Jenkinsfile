node {
    stage 'Checkout'
        checkout scm
    stage 'Prepare'
        bat 'dotnet restore'
    stage 'Build'
        bat "dotnet build -c Release"
    stage 'Test'
        bat "dotnet test -v detailed -c Release"
        }