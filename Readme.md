<h2> Pipeline design of Distributed Ansible ci-cd job configured using Jenkins-master-slave job </h2>

<ol type= "1">
  <li> The first step was to connect to our Jenkins UI using the public ip address and port 8080 of our Ansible controller in which jenkins has been already installed. </li> <br>
   <li> Once we have access to our Jenkins UI, we'll create and configure a pipeline job 
        In out pipeline job, we'll configure parameters like the log rotation, build triggers, the source code management tool and the repository url of our project. </li> <br>
 <li> We will then install some important plugins such as; Ansible, blue ocean, publish over ssh <br>
      We will then install maven as a global configuration tool.
 </li> <br>
 <li> Since we are running a Jenkins master-slave architecture, we'll then have to add a node which will act as a slave so as to reduce the stress on the jenkins master.       And that slave is an ec2 instance in which the java run time engine has been installed on, so that it can be able to communicate with the jenkins master  
  </li> <br>
<li> I'll have to move to the Jenkins file and define under agent, the label of my slave, so that all the stages of my pipeline will run on that slave </li>
  </ol>
  
