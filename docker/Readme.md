# How to run

1. build jenkins image form image folder. eg:
   ```text
  
   docker build -t demo/jenkins:0.1 .
    
   ```
2. run image. eg:
   ```text
   
   docker run --rm -p 8080:8080 -p 50000:50000 
   --group-add $(stat -c '%g' /var/run/docker.sock) 
   -v /workspace/jenkins/jenkins_home:/var/jenkins_home 
   -v /jenkins/docker/jcasc/:/workspace/jenkins/jcasc 
   -v /root/.m2:/root/.m2 
   -v /usr/bin/docker:/usr/bin/docker 
   -v /var/run/docker.sock:/var/run/docker.sock 
   -e CASC_JENKINS_CONFIG=/workspace/jenkins/jcasc 
   demo/jenkins:0.1
   
   ```
   
# More

add plugin define into plugins.txt. find plugin in https://plugins.jenkins.io/

folder no premisse. eg: chown -R 1000:1000 /var/jenkins_home