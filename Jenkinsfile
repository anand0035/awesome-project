pipeline{
    agent any
    environment {
            //Fastlane Environment Variables
           ANDROID_SDK_ROOT="/root/android-sdk-linux"
           APP_NAME = "DEMO_APP"
            LC_ALL = "en_US.UTF-8"
            LANG = "en_US.UTF-8"

        }

    stages
    {
        stage('npm install'){
            steps{
                sh 'npm install'
            }
        }
//         stage('testing your code'){
//             steps{
//                 bat 'npm run test'
//             }
//         }
        stage('build android'){
            steps{
                //sh "export ANDROID_SDK_ROOT=/root/android-sdk-linux"
                sh "chmod +x android/gradlew"
                sh "export ANDROID_SDK_ROOT"
                sh "/var/lib/gems/3.0.0/gems/fastlane-2.208.0/bin/fastlane android build"
                //sh "fastlane android build"
            }
        }
    }
}

