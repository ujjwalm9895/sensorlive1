# End-to-End Sensor Fault Detection System

This project delivers a complete pipeline for detecting faults in real-time sensor data. By integrating advanced machine learning models, robust data pipelines, and cloud-based deployment strategies, the system ensures accurate and efficient fault detection and management.

---

## **Key Features**
- **Real-time Fault Detection:** Employs machine learning models to identify sensor faults in real-time.
- **Comprehensive Pipeline:** Automates data ingestion, validation, transformation, and model training.
- **AWS Integration:** Utilizes AWS S3, ECR, and EC2 for seamless storage, model deployment, and scalability.
- **API Integration:** Provides real-time fault detection via FastAPI.
- **CI/CD Automation:** Ensures smooth development cycles with GitHub Actions and Docker.
- **Testing:** Implements robust testing using PyTest for pipeline reliability.

---

## **Technologies Used**

### **Programming and Frameworks:**
- Python
- FastAPI
- Machine Learning Libraries (Scikit-learn, Pandas, NumPy)

### **Deployment Tools:**
- Docker
- AWS CLI
- AWS ECR
- AWS EC2

### **Database and Storage:**
- MongoDB
- AWS S3

### **Version Control and CI/CD:**
- Git
- GitHub Actions

### **Testing:**
- PyTest

---

## **Pipeline Overview**

1. **Data Ingestion:**
   - Collects sensor data and stores it in MongoDB and AWS S3 for secure and scalable storage.

2. **Data Validation and Transformation:**
   - Validates incoming data for completeness and accuracy.
   - Transforms data into a suitable format for model training and inference.

3. **Model Training:**
   - Trains machine learning models to detect sensor faults with high accuracy.
   - Implements hyperparameter optimization for improved performance.

4. **Evaluation:**
   - Evaluates model performance using metrics like accuracy, precision, recall, and F1-score.

5. **Deployment:**
   - Packages the trained model in a Docker container.
   - Deploys the container on AWS EC2 for real-time inference.

6. **API Integration:**
   - Builds a FastAPI interface for users to query the system in real-time.

7. **CI/CD Integration:**
   - Automates build, test, and deployment pipelines using GitHub Actions and Docker.

8. **Testing:**
   - Ensures reliability and robustness with unit tests and integration tests using PyTest.

---

## **Results**
- Developed a scalable pipeline capable of handling large-scale sensor data.
- Achieved high accuracy in detecting sensor faults, ensuring system reliability.
- Enabled real-time inference and fault detection with FastAPI and AWS deployment.

---

## **How to Run the Project**

### **Prerequisites:**
- Python (v3.8+)
- AWS CLI configured
- Docker installed
- MongoDB configured
- Git and GitHub Actions setup

### **Steps:**

1. **Clone the Repository:**
   ```bash
   git clone [repository_url]
   cd [repository_folder]
   ```

2. **Set Up Environment:**
   ```bash
   python -m venv env
   source env/bin/activate  # On Windows: env\Scripts\activate
   pip install -r requirements.txt
   ```

3. **Configure AWS:**
   ```bash
   aws configure
   ```

4. **Run Data Pipeline:**
   ```bash
   python data_pipeline.py
   ```

5. **Train the Model:**
   ```bash
   python train.py
   ```

6. **Run Tests:**
   ```bash
   pytest tests/
   ```

7. **Build Docker Image:**
   ```bash
   docker build -t sensor-fault-detection .
   ```

8. **Deploy to AWS:**
   ```bash
   docker push [AWS_ECR_URI]
   aws ec2 run-instances --image-id [AMI_ID] --count 1 --instance-type t2.micro --key-name [KEY_PAIR] --security-groups [SECURITY_GROUP]
   ```

9. **Access API:**
   - Open the deployed FastAPI endpoint to query the system.

---

## **Future Enhancements**
- Integrate advanced anomaly detection algorithms for improved fault detection.
- Enhance scalability for handling a larger number of sensors.
- Add Explainable AI (XAI) techniques to interpret fault predictions.

---

## **Contributors**
- **Ujjwal Madawat**

For any queries, feel free to reach out at Ujjwalm9895@gmail.com.

