📦 HELLO-JAVA-MAVEN 🚀
A simple Java Hello World application built and packaged using Maven, automated with Jenkins.
This is a beginner-friendly CI/CD pipeline demonstration.

📚 Project Structure

HELLO-JAVA-MAVEN/
├── pom.xml
└── src/
    └── main/
        └── java/
            └── HelloWorld.java


🎯 Objective
✅ Create a simple Java Hello World application
✅ Build the project using Maven
✅ Run the build job using Jenkins
✅ View build logs and artifacts



🛠️ Tools Used
📦 Jenkins (installed via system package or Docker)
```
sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins
```


☕ Java JDK 17
```
 sudo apt install openjdk-17-jre-headless
 ```

🐘 Apache Maven
```
sudo apt install maven -y
```

🐙 Git 



🚀 How to Run This Project
1️⃣ Clone the Repo (if applicable)
```
git clone [<your-repo-url>](https://github.com/SuryaSJV/HELLO-JAVA-MAVEN.git)
```
2️⃣ Move the Project to Jenkins Workspace
```
sudo mv /home/surya/HELLO-JAVA-MAVEN /var/lib/jenkins/
sudo chown -R jenkins:jenkins /var/lib/jenkins/HELLO-JAVA-MAVEN
```
3️⃣ Create a Jenkins Freestyle Job
-Go to Jenkins Dashboard

-Click on New Item

-Enter item name: HELLO-JAVA-MAVEN

-Select Freestyle project and click OK

4️⃣ Configure the Job
In Build section → Invoke top-level Maven targets

Set:
Goals: clean install
POM: /var/lib/jenkins/HELLO-JAVA-MAVEN/pom.xml

Click Save

![Image](https://github.com/user-attachments/assets/6261a655-5481-4c84-82fd-835f53d96df8)

![Image](https://github.com/user-attachments/assets/c4cdeb61-4efa-4340-a270-33117d383d61)

5️⃣ Build the Project
Click Build Now

Wait for build to complete

Go to Console Output to view logs

✅ You should see a BUILD SUCCESS message at the end.

![Image](https://github.com/user-attachments/assets/90bb2266-3e5d-4aa2-8365-c4ef9ca6067e)

![Image](https://github.com/user-attachments/assets/c1428338-06a5-4d43-847d-11374f0565d6)




