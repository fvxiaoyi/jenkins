# How to run

1. build jenkins image form image folder. eg:
   ```text
  
   docker build -t demo/jenkins:0.1 .
    
   ```
2. run image. eg:
   ```text
   
   docker run --rm -p 8080:8080 -p 50000:50000 
   -v /workspace/jenkins/jenkins-data:/var/jenkins_home 
   -v /workspace/jenkins/jcasc:/jcasc 
   -e CASC_JENKINS_CONFIG=/jcasc 
   demo/jenkins:0.1 
   
   ```
   
# More

add plugin define into plugins.txt. find plugin in https://plugins.jenkins.io/
