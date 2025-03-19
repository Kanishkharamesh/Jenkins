# Jenkins Pipeline Setup

## Prerequisites  

Ensure you have the following before proceeding:  
- **Jenkins** installed and running  
- **GitHub repository** with required files  
- **Docker** installed (if using containerized applications)  

## Steps to Set Up a Jenkins Pipeline  

### 1. Create a New Project in Jenkins  
- Open Jenkins and click on **"New Item"**.  
- Enter a name for your project.  
- Select **"Pipeline"** as the project type.  
- Click **"OK"** to continue.  

### 2. Configure the Pipeline  
- In the **General** tab, scroll down to the **Pipeline** section.  
- Under **Definition**, choose **"Pipeline script from SCM"**.  

### 3. Link the Pipeline to GitHub  
- In the **SCM** field, select **"Git"**.  
- Enter your **GitHub repository URL**.  

### 4. Ensure the Repository Contains Essential Files  
Your repository must include the following files:  
- **`app.py`** – The main application script.  
- **`Dockerfile`** – Defines instructions to build a Docker image.  
- **`docker-compose.yml`** – Manages container orchestration.  
- **`Jenkinsfile`** – Specifies pipeline stages and execution.  
- **`requirements.txt`** – Lists application dependencies.  

### 5. Save and Trigger the Build  
- Click **"Save"** to apply the configuration.  
- On the project page, select **"Build Now"** to start the pipeline.  

### 6. Monitor the Build Process  
- Check the **Build History** panel on the left side for progress.  
- Click on the latest build (#1, #2, #3 etc.) and open **"Console Output"** to view logs and results.  
