pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo "Provider: ${params.Provider}"
                def fileList = []
                def workspaceDir = pwd() // Get current directory (WORKSPACE)

                new File(workspaceDir).eachFile { file ->
                    if (file.isFile()) {
                        fileList.add(file.getName())
                    }
                }

                return fileList
            }
        }
    }
}
