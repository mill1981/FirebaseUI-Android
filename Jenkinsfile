def gradle(command) {
    sh "./gradlew ${command}"
}

node('master') {
	checkout scm
	gradle 'assembleDebug check jacocoTestReport'
}