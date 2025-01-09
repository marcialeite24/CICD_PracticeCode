# Create a base pipeline

This folder holds the files for the lab _Create a Base Pipeline_ which is part of the **IBM-CD0215EN-Skills Network Introduction to CI/CD** course.


Step 1: Create an echo Task

Apply it to the cluster: 
```bash
kubectl apply -f tasks.yaml
```

Step 2: Create a hello-pipeline Pipeline
Apply it to the cluster: 
```bash
kubectl apply -f pipeline.yaml
```

Step 3: Run the hello-pipeline
Run the pipeline using the Tekton CLI:
```bash
tkn pipeline start --showlog hello-pipeline
```

Step 4: Add a parameter to the task
Apply the new task definition to the cluster:
```bash
kubectl apply -f tasks.yaml
```

Step 5: Update the hello-pipeline
Apply it to the cluster:
```bash
kubectl apply -f pipeline.yaml
```

Step 6: Run the message-pipeline
Run the pipeline using the Tekton CLI:
```bash
tkn pipeline start hello-pipeline \
    --showlog  \
    -p message="Hello Tekton!"
```

Step 7: Create a checkout Task
Apply it to the cluster:
```bash
kubectl apply -f tasks.yaml
```

Step 8: Create the cd-pipeline Pipeline
Apply it to the cluster:
```bash
kubectl apply -f pipeline.yaml
```

Step 9: Run the cd-pipeline
Run the pipeline using the Tekton CLI:
```bash
tkn pipeline start cd-pipeline \
    --showlog \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch="main"
```

Step 10: Fill Out cd-pipeline with Placeholders
Apply it to the cluster:
```bash
kubectl apply -f pipeline.yaml
```

Step 11: Run the cd-pipeline
Run the pipeline using the Tekton CLI:
```bash
tkn pipeline start cd-pipeline \
    --showlog \
    -p repo-url="https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode.git" \
    -p branch="main"
```