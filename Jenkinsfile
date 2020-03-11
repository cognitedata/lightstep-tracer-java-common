@Library('jenkins-helpers@v0.1.39')

def label = "jonas-test-${UUID.randomUUID().toString()}"

podTemplate(
    label: label,
    annotations: [
	podAnnotation(key: "jenkins/build-url", value: env.BUILD_URL ?: ""),
	podAnnotation(key: "jenkins/github-pr-url", value: env.CHANGE_URL ?: ""),
    ],
)
{
    node(label) {
	sh('echo shouldnotprint')
    }
}
