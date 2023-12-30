node('slv2') {
    stage('Download') {
    git branch: 'dev', url: 'https://github.com/venkat9822891/my-project-28.git'
                      }
    stage('Convert Artifacts') {
    sh 'mvn package'
                               }
    stage('Deploy into the container') {
    deploy adapters: [tomcat9(credentialsId: '9a4b90b1-2631-4f93-911b-b8591f1f5eb5', path: '', url: 'http://172.31.38.175:8080')], contextPath: '/devapp', war: '**/*.war'
                                       }
   
    }
