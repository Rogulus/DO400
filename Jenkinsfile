pipeline {
	agent { node { label 'pipeline-as-code-node'}}
	stages {
		stage ('Checkout') {
			steps {
				git url: 'https://github.com/Rogulus/DO400'
			}
		}
		stage ('Succ Test') {
			steps {
				sh './succ_test.sh'
			}
		}
		stage ('Fail Test') {
			steps {
				sh './fail_test.sh'
			}
		}
	}
}
