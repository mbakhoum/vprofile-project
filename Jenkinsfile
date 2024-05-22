pipeline{
    agent any
    tools{
        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment{
        NEXUSPORT = '8081'
        NEXUSIP = '172.31.20.128'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        SNAP_REPO = 'vprofile-snapshot'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'

    }
    stages{
        stage('Build'){
            steps{
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}