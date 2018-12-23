pipeline {
  agent any

  options {
    skipDefaultCheckout true
  }
stages{
stage('Checkout') {
  steps {
    checkout([
        $class: 'GitSCM',
        branches: scm.branches,
        extensions: scm.extensions + [[$class: 'LocalBranch'], [$class: 'CleanCheckout']],
        userRemoteConfigs: scm.userRemoteConfigs
    ])
  }
}
}

}
