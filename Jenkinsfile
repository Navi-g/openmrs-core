node('JAVA') {
    stage('scm') {
        git 'https://github.com/Navi-g/openmrs-core.git'
    }
    stage('Build'){
        sh 'mvn clean package'
    }
    stage('POST'){
        junit '**/TEST-*.xml'
        archive '**/*.war'
    }
}