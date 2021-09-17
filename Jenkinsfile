node {
    stage 'Checkout'
        checkout scm

    stage 'Prepare'
        bat 'nuget restore "APIMATICCalculator.sln"'

    stage 'Build'
        bat "dotnet build -c Release \"APIMATICCalculator.sln\""
        stage 'Test'
        bat "dotnet test -v detailed -c Release APIMATICCalculator.Tests\\bin\\Release\\netcoreapp3.0\\APIMATICCalculator.Tests.dll"            
     }