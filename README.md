📄 Overview

This project focuses on containerizing a simple Node.js calculator microservice and publishing it to a private Artifact Registry repository on Google Cloud Platform (GCP).
The microservice supports basic operations like addition, subtraction, multiplication, division, and modulus.

By completing this task, production deployment practices are demonstrated, ensuring that the application is ready to be pulled and deployed in any cloud environment.

🛠 Project Structure
```
week5taskD/
├── Dockerfile             # Defines container instructions for Node.js app
├── package.json           # Project dependencies
├── package-lock.json      # Lock file for dependency versions
├── test.js                # Microservice source code
├── .gitignore             # Specifies ignored files
└── README.md              # Project documentation (this file)
```
⚙️ How to Build and Publish

1️⃣ Clone the Repository
```
git clone https://github.com/SatyamRaina/sit323-2025-prac5d.git
cd sit323-2025-prac5d/week5taskD
```
2️⃣ Build Docker Image
```
docker build -t week05-calculator .
```
3️⃣ Authenticate Docker with GCP Artifact Registry
```
gcloud auth configure-docker australia-southeast2-docker.pkg.dev
```
This step links Docker with your private Artifact Registry repository.
4️⃣ Tag the Docker Image
```
docker tag week05-calculator australia-southeast2-docker.pkg.dev/sit323-25t1-raina-fbe502e/calculator-repo/week05-calculator
```
5️⃣ Push Image to Artifact Registry
```
docker push australia-southeast2-docker.pkg.dev/sit323-25t1-raina-fbe502e/calculator-repo/week05-calculator
```
The image is now published privately on Google Cloud.

📸 Included Screenshot

1. Artifact Registry view showing the week05-calculator image successfully uploaded.
2. Verified that the repository is in region australia-southeast2.

🎯 Learning Outcomes

1. Gained hands-on experience in containerizing microservices.
2. Understood authentication and configuration for private container registries.
3. Successfully published a production-ready Docker image to GCP Artifact Registry.
   
🔥 Future Improvements (Optional)

1. Implement CI/CD pipeline to automate image builds and push to Artifact Registry.
2. Introduce version tagging for better microservice release management.
3. Set up vulnerability scanning using GCP's Artifact Analysis tool.
   
👨‍💻 Author

Satyam Raina
Bachelor of Software Engineering (Honours) – Cloud Computing Major
Deakin University, Australia
