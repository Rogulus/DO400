pipeline {
	agent any
	parameters {
		booleanParam (name: 'RUN_FRONTEND_TESTS', defaultValue: true)
	}
	stages {
		stage ('Checkout') {
			steps {
				git url: 'https://github.com/Rogulus/DO400'
			}
		}
		stage ('Run tests') {
			parallel {
				stage ('Backend tests') {
					steps {
						sh './tests/backend/echo'
					}
				}
				stage ('Frontend tests') {
					when { expression {params.RUN_FRONTEND_TESTS}}
					steps {
						sh './tests/frontend/echo'
					}
				}
			}
		}
	}
}
