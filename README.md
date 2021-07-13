**Project Setup**
1. make vagrant-provision
2. Go to http://10.2.2.25 on your browser
3. Create a test project and generate an access token for it (http://10.2.2.25/projects/create)
4. Set your project name in file ./sonar-project.properties
sonar.projectKey=<project_name>

**Using project**
1. Use docker and default admin credentials for connecting to sonarqube site (IP - 10.2.2.25)
2. docker run --rm -e SONAR_HOST_URL="http://10.2.2.25" -e SONAR_LOGIN="admin" -e SONAR_PASSWORD="admin" -v "<full_path_to_folder_project>" sonarsource/sonar-scanner-cli