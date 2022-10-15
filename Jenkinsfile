pipeline {
  agent {
    label "kube-agent"
  }

  stages {
    stage('Test') {
      steps {
        container('webapp-agent') {
            sh """
            ls -la /home/jenkins/agent
            cat /etc/os-release
            whoami
            uname -a
        """
        }
      }
    }
    stage('Build') {
      steps {
        container('kaniko') {
            sh """
            ls -la
        """
        }
      }
    }
  }
}
