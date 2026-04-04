pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/2025sl93076-BITS-DEVOPS/labsheet--2025sl93076-.git'
            }
        }

        stage('Build') {
            steps {
                echo "Build stage - nothing to compile for Python"
            }
        }

        stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
import calculator

assert calculator.add(2,3) == 5
assert calculator.subtract(5,2) == 3
assert calculator.multiply(2,3) == 6
assert calculator.divide(6,2) == 3

print("All tests passed!")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy stage completed"
            }
        }
    }
}
