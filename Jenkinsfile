@Library('jenkins-library@1.0.4') _

def tasks = [:]
tasks["offchain"] = {
    stage ("Build Kaiko Pricefeed"){
        def nativeImage = buildSimpleDocker_v2(dockerfileDir: 'offchain-computing',
                dockerImageRepositoryName: 'offchain-tee-kaiko-pricefeed', imageprivacy: 'public')
        sconeBuildAllTee(nativeImage: nativeImage, targetImageRepositoryName: 'offchain-tee-kaiko-pricefeed',
                sconifyArgsPath: 'offchain-computing/sconify.args')
    }
}
parallel tasks