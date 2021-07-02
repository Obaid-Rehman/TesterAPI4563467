node {
    stage 'Checkout'
        checkout scm

    stage 'Prepare'
        bat 'nuget restore "APIMATICCalculator.sln"'
        bat 'nuget install NUnit.Runners -Version 3.2.1 -OutputDirectory testrunner'

    stage 'Build'
        bat "dotnet build -c Release \"APIMATICCalculator.sln\""
        stage 'Test'
        bat "dotnet test -v detailed -c Release APIMATICCalculator.Tests\\bin\\Release\\netcoreapp3.0\\APIMATICCalculator.Tests.dll"            
     }