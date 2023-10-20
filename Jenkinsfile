pipeline {
    agent {
        label 'slave'
    }
	environment {
        PATH = "/home/jenkins/.local/bin:$PATH"
	}
    stages {
        stage('Download role') {
            steps {
                git branch: 'main', credentialsId: '4ba6333d-5fac-4011-b2d3-db47d29a74ca', url: 'https://github.com/Midzaru2011/vector-role'
                }
            }
        stage('Install molecule') {
            steps {
                sh 'pip3 install molecule==3.5.2 molecule-docker'
            }
        }
        stage('add community.docker') {
            steps {
                sh 'ansible-galaxy collection install community.docker'
            }
        }
        stage('Molecule test') {
            steps {
                sh 'molecule test'
			}
		}
	}
}
