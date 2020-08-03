
pipeline {
    // 没有 agent 指令的话, 声明式流水线不仅无效, 它也不可能完成任何工作
    agent any
        // 使用全局定义工具
        tools {
            maven 'maven'
            jdk 'jdk'
        }
        stages {
            stage('build') {
                steps {
                    echo 'Building..'
                    // 输出路径
                    sh 'pwd'
                    sh 'mvn --version'
                    sh 'java -version'
                }
            }
        }
}