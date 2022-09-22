pipeline {
    agent any
    stages{
        stage("Connection"){
            steps{
                deleteDir()
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'aed9f4e6-2dc0-458b-bc8c-0280262644c5', url: 'git@gitlab:pawelkur/imageio.git']]])
                }
        }
        stage("maven_install"){
            steps{
                sh "mvn install"
            }

        }
    }    
}

