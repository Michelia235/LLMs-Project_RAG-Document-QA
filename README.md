# LLMs-Project_RAG-Document-QA

## Deploy Chatbot using Ngrok

Ngrok is a tool that creates a tunnel between your localhost and the internet, similar to localtunnel. Below are the steps to deploy your chatbot using Ngrok:

### Step 1: Create a Ngrok Account

- Go to [Ngrok](https://ngrok.com/), create an account, and log in.

### Step 2: Get Your Authtoken

- Navigate to the **Your Authtoken** section and copy your authtoken.
  ![Auth Token](https://scontent.fsgn5-8.fna.fbcdn.net/v/t39.30808-6/449697964_337080206107141_2878106079208042090_n.jpg?_nc_cat=109&ccb=1-7&_nc_sid=aa7b47&_nc_eui2=AeH2mpXjAN3vFotM0pLE6jmOotm5iLxqxSyi2bmIvGrFLJBkwD-nHc5MkoQFBFrbafE1GvgYFfi4kxN7aOMm5xWk&_nc_ohc=EiwMEdpMZLYQ7kNvgFHIfU7&_nc_ht=scontent.fsgn5-8.fna&oh=00_AYAYPlfn1rOPaoIKMmeICi7RMbpupFgc3Z50QvJ4qDmjmg&oe=6688E677)

### Step 3: Set Up Ngrok in Your Environment

- Open your development environment and install Ngrok by running the following command:
  ```python
  !pip install pyngrok -q


### Step 4: Configure Ngrok with Your Authtoken

- Run the following commands to configure Ngrok with your authtoken:
  ```python
  from pyngrok import ngrok

  !ngrok config add-authtoken YOUR_AUTHTOKEN
  ```

  ![Ngrok Setup](https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/449215990_337080236107138_4661462147290681086_n.jpg?_nc_cat=107&ccb=1-7&_nc_sid=aa7b47&_nc_eui2=AeHpPyAyMCCxdHlACrk8Jf5MpaqHxjRamxulqofGNFqbG1YcYiCuUD_bxMcvu19sb9fxoLVz4Cn37WMUeKYLFd62&_nc_ohc=Q9-74EHkyWYQ7kNvgFfNJNf&_nc_ht=scontent.fsgn5-10.fna&oh=00_AYBniE3J2WJUAZx3GBVgmPU5DJYQDlP8xsmrjfrWqDPYqg&oe=6688DD38)

### Step 5: Deploy Your Application

- Run your application and start Ngrok to create a public URL:
  ```python
  public_url = ngrok.connect(8000).public_url
  ```

- Then run your application with Chainlit:
  ```bash
  !chainlit run app.py
  ```

### Step 6: Access Your Application

- Wait until the app.py finishes running (you will see a blue message saying "Your app is available at http://localhost:8000").
- Go to the public URL provided by Ngrok and see the result!

  ![Ngrok Running](https://scontent.fsgn5-14.fna.fbcdn.net/v/t39.30808-6/449697117_337080266107135_988633332718854828_n.jpg?_nc_cat=106&ccb=1-7&_nc_sid=aa7b47&_nc_eui2=AeEUKNBvHxtQped0Mtz_VgwqC-xZBm4QdGQL7FkGbhB0ZHujzpMrH3Q5h942AbL95N0VWgyb5-iSY0EgQhx9R5LM&_nc_ohc=xw1tuU1IZUoQ7kNvgGgd7pA&_nc_ht=scontent.fsgn5-14.fna&oh=00_AYCt-wTMGTCUO4yCoe7fUIphaVV7h1SVl8owoO9Jrbg7tQ&oe=6688CA12)

### Step7: "Instructions for using the website."
- After accessing the website, you proceed to upload a PDF file. Once the file has been uploaded, you can ask questions related to that file.

!["Chanlit Interface"](![image](https://github.com/Michelia235/LLMs-Project_RAG-Document-QA/assets/171731506/326be203-d963-4b2f-b94e-64a65d2559cd)

