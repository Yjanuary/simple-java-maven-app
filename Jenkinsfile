node{
    stage('git clone'){
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'bdcdd49a-86ed-426f-b740-fb1606f0b7d0', url: 'http://192.168.126.160:8888/root/jenkins-demo.git']]])
    }
    stage('mvn test'){
        withMaven(maven: 'maven') {
                sh "mvn test"
        }
    }
    stage('mvn build'){
        withMaven(maven: 'maven') {
                sh "mvn clean install -Dmaven.test.skip=true"
        }
    }
}