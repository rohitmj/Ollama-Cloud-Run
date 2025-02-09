# Running Open LLMs with Ollama on Google Cloud Run

## Introduction
This guide provides a step-by-step walkthrough of deploying an open Large Language Model (LLM) using **Ollama** on **Google Cloud Run**. The tutorial is based on a blog post by **Geshan Manandhar**, which can be found [here](https://geshan.com.np/blog/2025/01/ollama-google-cloud-run/).

I followed the instructions outlined in the tutorial and successfully deployed the project. Below is a detailed breakdown of the process, including screenshots of my successful implementation.

---

## Step 1: Creating a Google Cloud Storage Bucket
The first step was to create a **Cloud Storage Bucket** named `ollama-gemma2-2bx` to store necessary files.

![Bucket Creation](https://github.com/user-attachments/assets/36484d7b-4651-43ac-8d8a-4feb7cc47fe8)

---

## Step 2: Deploying Ollama on Google Cloud Run
After setting up the bucket, I proceeded to deploy **Ollama** on **Google Cloud Run**. This involved:
- Creating a Cloud Run service.
- Deploying the service with the necessary configurations.

![Cloud Run Deployment](https://github.com/user-attachments/assets/4a427ac4-a00a-4b0c-8889-b440d1b05409)

Once deployed, I accessed the **service URL**, which confirmed that the deployment was successful.

![Service URL Confirmation](https://github.com/user-attachments/assets/5844a0da-6504-42cb-9c87-176ba1df41c3)

---

## Step 3: Downloading Gemma 2:2B
After deployment, I attempted to download the **Gemma 2:2B** model in **Cloud Shell**. However, this step failed due to **insufficient memory**.

![Download Failure](https://github.com/user-attachments/assets/9ed09086-7495-4791-a5f0-cb359163928d)

---

## Step 4: Using a Smaller LLM Model
Since **Gemma 2:2B** required more memory than available, I opted for a smaller LLM, **SmolLM 2:135M**, which successfully ran without memory issues.

![Successful Deployment of SmolLM]![image](https://github.com/user-attachments/assets/1dbd384a-88f3-4797-b849-69fc47a3485c)


---

## Conclusion
By following **Geshan Manandhar’s tutorial**, I was able to successfully deploy **Ollama** on **Google Cloud Run** and run a lightweight LLM. The process highlighted key challenges such as **memory constraints** when using larger models and provided insights into optimizing deployments by selecting appropriate models.

If you are interested in running **Ollama** on **Google Cloud Run**, I highly recommend checking out the [original tutorial](https://geshan.com.np/blog/2025/01/ollama-google-cloud-run/).

For further questions or discussions, feel free to connect with me on [GitHub](https://github.com/rohitmj).

