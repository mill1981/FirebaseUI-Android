def gradle(command) {
    sh "./gradlew ${command}"
}

node('master') {
	stage('Sync Source Code') {
		checkout scm
	}
	stage('Gradle Build') {
		gradle 'assembleDebug check jacocoTestReport'
	}
	stage('Archive build output') {
		archive '**/*.apk'
	}
}