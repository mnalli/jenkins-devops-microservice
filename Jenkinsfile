pipeline {
	agent any

	stages {
		stage("Build") {
			steps {
				echo "====++++executing Build++++===="
				echo "Build"
			}
		}
		stage("Test") {
			steps {
				echo "====++++executing Test++++===="
				echo "Test"
			}
		}
		stage("Integration Test") {
			steps {
				echo "====++++executing Integration Test++++===="
				echo "Integration Test"
			}
		}
	}

	post {
		// after all stages are executed
		always {
			echo "Always"
		}
		success {
			echo "Success"
		}
		failure {
			echo "Failure"
		}
		unstable {
			// some test has failed
			echo "Unstable"
		}
		changed {
			// the build status has changed
			echo "Changed"
		}
	}
}
