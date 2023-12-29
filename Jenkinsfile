node {
    stage('Download') {
    git branch: 'dev', url: 'https://github.com/venkat9822891/my-project-28.git'
                      }
    stage('Convert Artifacts') {
    sh 'mvn package'
                               }
    stage('Deploy into the container') {
    deploy adapters: [tomcat9(credentialsId: '80cfc1fd-0b6e-4813-b27a-ad2ac8305115', path: '', url: 'http://13.232.145.195:8080')], contextPath: '/devapp', war: '**/*.war'
                                       }
   
    }
