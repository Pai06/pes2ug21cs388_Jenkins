pipeline{
  agent any
  stages {
//          stage('Clone repository'){
 //           steps {
  //            checkout([$class: 'GitSCM',
   //           branches: [[name: '*/main']],
     //         userRemoteConfigs: [[url: 'https://github.com/Pai06/pes2ug21cs388_Jenkins.git']]])
       //     }
         // }
    stage('Build'){
        steps {
          build 'pes2ug21cs397-1'
          sh 'g++ sample.cpp -o output'
        }
    }
    stage('Test') {
      steps {
        sh './output'
        }
    }
    stage('Deploy') {
        steps {
            echo 'deploy'
        }
    }
}
post{
  failure{
    error 'Pipeline failed'
  }
}
}
