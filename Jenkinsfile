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
    publishers {
        extendedEmail {
            recipientList('me@alma.org')
            defaultSubject('Oops')
            defaultContent('Something broken')
            contentType('text/html')
            triggers {
                failure {
                    subject('Subject FAILURE')
                    content('Body')
                    sendTo {
                        developers()
                        requester()
                        culprits()
                    }
                }
            }
        }
    }
}
