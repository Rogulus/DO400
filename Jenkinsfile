pipeline {
	agent any
	stages {
		stage ('Checkout') {
			steps {
				git url: 'https://github.com/Rogulus/DO400'
			}
		}
		stage ('Backend tests') {
			steps {
				sh './tests/backend/echo'
			}
		}
		stage ('Frontend tests') {
			steps {
				sh './tests/frontend/echo'
			}
		}
	}
}
