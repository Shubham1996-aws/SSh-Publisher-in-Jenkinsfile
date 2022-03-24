pipeline {
    agent any

    stages {
        stage('Git Clone') {
            steps {
                git 'https://github.com/Shubham1996-aws/nodejs-app-mss.git'
            }
        }
        
        stage('Copy Code to Server') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'Wordpress-Server', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
