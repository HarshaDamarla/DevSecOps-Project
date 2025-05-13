pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        script {
          def buildTime = new Date().format("yyyy-MM-dd HH:mm:ss")
          echo "Build triggered at: ${buildTime}"
        }
      }
    }
  



    stage('Unit and Integration Tests') {
      steps {
        echo 'Stage 2: Run unit and integration tests using JUnit or TestNG'
        echo 'Regression testing is also done'
        // Example: sh 'mvn test'
      }
    }

    stage('Code Analysis') {
      steps {
        echo 'Stage 3: Analyze code quality using SonarCloud'
        echo 'code analysis is done'
        // Example: sh 'sonar-scanner'
      }
    }

    stage('Security Scan') {
      steps {
        echo 'Stage 4: Perform a security scan using Snyk or npm audit'
        // Example: sh 'npm audit'
      }
    }

    stage('Deploy to Staging') {
      steps {
        echo 'Stage 5: Deploy application to a staging server (e.g., AWS EC2)'
        // Example: sh 'scp target/app.jar ec2-user@staging:/app/'
      }
    }

    stage('Integration Tests on Staging') {
      steps {
        echo 'Stage 6: Run integration tests on staging environment'
        // Example: sh 'curl http://staging-server/health'
      }
    }

    stage('Deploy to Production') {
      steps {
        echo 'Stage 7: Deploy application to production environment'
        // Example: sh 'scp target/app.jar ec2-user@prod:/app/'
      }
    }
  }
}
