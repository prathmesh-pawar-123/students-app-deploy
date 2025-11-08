# 🎓 Student App Deployment using Java with CI/CD Pipeline

## 🚀 Project Overview
This project demonstrates how to deploy a *Java-based Student Application* using a *CI/CD pipeline* with *Jenkins, **GitHub, and **Tomcat Server* on *AWS EC2 instances*.

The goal of this project is to automate the build, test, and deployment process of a Java web application.

---

## 🧩 Technologies Used
- *Java*  
- *Apache Tomcat*  
- *Jenkins*  
- *Git & GitHub*  
- *AWS EC2 (Ubuntu)*  
- *Maven*  
- *Web Browser (for app access)*  

---

## ⚙ Project Flow / Steps

### 1️⃣ Launch EC2 Instances
- Launch an *Ubuntu EC2 instance* from AWS console.  
- Connect via SSH using terminal or PuTTY.  
- Install Java, Git, Jenkins, and Tomcat on the instance.
- - sudo apt update -y
- - sudo apt install openjdk-11-jdk git maven -y

-

- Verify Jenkins by accessing:

http://<public-ip>:8080
- -i[] (./img/![alt text](<img/Screenshot (14).png>))

### 2️⃣ Setup Apache Tomcat Server
- Install and configure *Tomcat server*.  
- Deploy a sample Java .war file manually first to test the setup.
- - sudo hostnamectl hostname tomcat
- - sudo apt update 
- - sudo apt install tomcat10 -y
- - sudo systemctl start tomcat10
- - sudo systemctl enable tomcat10

- Access it using:

http://<public-ip>:8080/StudentApp

i[] (./img/![alt text](<img/Screenshot (15).png>))

### 3️⃣ Create GitHub Repository
- Create a new repository named *student-app-java*.  
- Push your Java project files (pom.xml, src/, etc.) to the repo.  

![] (./img/![alt text](<img/Screenshot (16).png>)) 

### 4️⃣ Create a New Jenkins Job
- - Open your jenkins dashboard in your browser.
- - Click on "New Item" from the jenkins home page.
- - Enter a name for your job : student-app-deploy.
- - select "pipeline" and click OK.
- - Scroll down to the Pipeline section.
- - under defination,select "Pipeline script from SCM".
- - Choose SCM = Git.
- - Paste your Github repository URL.
- - Select the branch name (main or master).
- - click save.

![] (./img![alt text](<img/Screenshot (17).png>)/)

![] (./img/![alt text](<img/Screenshot (18).png>))

### 5️⃣ Check Console Output
- Click on *Build Now* and check *Console Output*.  
- Jenkins will automatically:  
- Pull code from GitHub  
- Build using Maven  
- Deploy .war file to Tomcat webapps folder 
- - ![] (./img/![alt text](<img/Screenshot (19).png>)) 

### 6️⃣ Job Successfully Executed
- Once the build is successful, Jenkins shows *“SUCCESS”* message in green.  
- Verify the deployment on your Tomcat server.
- - ![] (./img/![alt text](<img/Screenshot (20).png>))

### 7️⃣ Final Output
- Open your browser and visit:

http://<EC2-public-ip>:8080
![] (./img/![alt text](<img/Screenshot (21).png>))

- You’ll see your *Student Management Application* live 🎉  


---



## 🏁 Result
✅ Successfully implemented a *Java-based Student App* deployed using *CI/CD pipeline* through *Jenkins and Tomcat on AWS EC2*.

---

## 🧠 Learning Outcomes
- Understanding of CI/CD concepts  
- Jenkins pipeline automation  
- Continuous deployment on Tomcat server  
- Integration of GitHub with Jenkins
