pipeline {
    agent any
    tools { 
        maven 'maven-3' 
    }
    stages {
        stage ('Build') {
            when {
                branch 'feature/*'
            }
            steps {
                sh 'mvn clean install'
            }
        }
        stage ('Build & Deploy artifact') {
            when {
                branch 'master'
            }
            steps {
                checkout([
                $class: 'GitSCM', 
                extensions: [
                  [$class: 'LocalBranch'],
                  [$class: 'UserExclusion', excludedUsers: 'idugalic-namics']
                 ]])
                script{
                    sh 'git config --global user.email "ivan.dugalic@namics.com"'
                    sh 'git config --global user.name "idugalic-namics"'
                    def pom = readMavenPom file: 'pom.xml'
                    def version = pom.version.replace("-SNAPSHOT", ".${currentBuild.number}")
                    sh "mvn -DreleaseVersion=${version} -DdevelopmentVersion=${pom.version} release:clean release:prepare release:perform -B"
                }
            }
        }
    }
}
