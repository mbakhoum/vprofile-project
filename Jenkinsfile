pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment{
        NEXUSPORT = '8081'
        NEXUSIP = '172.31.20.128'
        NEXUS-GRP-REPO = 'vpro-maven-group'
        SNAP-REPO = 'vprofile-snapshot'
        RELEASE-REPO = 'vprofile-release'
        CENTRAL-REPO = 'vpro-maven-central'
        NEXUS-USER = 'admin'
        NEXUS-PASS = 'admin123'

    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}