job('gradle-jenkins-tutorial') {
    description("Gradle Jenkins Tutorial job")
    scm {
        github('sotcsa/gradle-jenkins-tutorial', 'master')
    }
    steps {
        shell('echo START')
        gradle('clean build')
    }
    triggers {
        scm('H/* * * * *')
    }
}
