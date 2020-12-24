pipeline {
  agent {
    dockerfile {
      dir 'build'
      args '--security-opt seccomp=unconfined --security-opt label=disable --cap-add SYS_ADMIN --env STORAGE_DRIVER=vfs'
    }
  }

  stages {
    stage('Build') {
      steps {
        sh "echo Test podman"
        sh "podman run docker.io/library/alpine cat /etc/os-release"
      }
    }

  }
}

