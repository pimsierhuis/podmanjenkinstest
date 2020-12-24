pipeline {
  agent {
    dockerfile {
      dir 'build'
//      args '--security-opt seccomp=unconfined --security-opt label=disable --cap-add SYS_ADMIN --env STORAGE_DRIVER=vfs'
      args '--security-opt seccomp=unconfined --security-opt label=disable --cap-add SYS_ADMIN --device /dev/fuse' 
      additionalBuildArgs '--security-opt seccomp=unconfined --security-opt label=disable --cap-add SYS_ADMIN --device /dev/fuse'
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

