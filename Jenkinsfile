node{
    properties([parameters([choice(choices: 'test', description: '', name: 'Env')]), pipelineTriggers([])])
    stage('Pull from git hub'){
      git 'https://github.com/GauravKumarQA/AutomationFrameworkUsingTestNG'
    }
    stage('Maven test'){
        def mavenHome = tool name: 'M2_HOME', type: 'maven'
        bat "${mavenHome}/bin/mvn clean test -Denv=Env  -DbrowserName=chrome"
    }
}
