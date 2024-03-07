pipeline {
	agent any
	// agent { docker { image 'maven:3.6.3' } }

	stages {
		stage("Build") {
			steps {
				echo "====++++executing Build++++===="
				// sh "mvn --version"
				echo "Build"
				echo "PATH: $PATH"
				echo "BUILD_NUMBER: $env.BUILD_NUMBER"
				echo "BUILD_ID: $env.BUILD_ID"
				echo "JOB_NAME: $env.JOB_NAME"
				echo "BUILD_TAG: $env.BUILD_TAG"
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
