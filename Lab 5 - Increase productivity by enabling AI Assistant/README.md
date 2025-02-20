![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/6d6c7ee8-7a42-456f-8a2e-5b60b14f8f04)# AI Assistant

## Setup watsonx.assistant platform

1. Go to resources list in IBM Cloud --> type "assistant" in search field --> click on service watsonx.assistant
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/9c2ff4d3-8a28-4982-89ff-5e174c016c90)

2. Click Launch watsonx.assistant button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/f8e51ff5-3ece-4809-9b41-0a82b96585bc)

3. Create new chatbot --> fill your chatbot name --> set language to Another language --> Click Create button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/2104407d-e0a6-4fa0-a8dd-f23fc5fccffe)

## Create basic action

1. Click Create action button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/902a2d1a-efbd-4bda-80f1-f35fdaa353e4)

2. Type "Introduction" as conversation starter
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/c876a39c-ece2-4235-a094-72e7e6eec83d)

3. Type text below in "Assistant says" text area

```
Hi, may I know your name first ?
```

![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/adee31b4-97b5-49d9-a8ab-c28a7995df12)

4. Click Define customer response --> select Free text
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/7b51c0e3-459b-45a6-962f-f0469a3ae023)

5. Click New step button --> type "Hi $" until you can see the picture below
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/6cab8703-77df-4c10-9b12-ad200fc2b79c)

6. Click Action step variable --> Click "Hi, may I know your name first" --> this is to get response from your previous step
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/d12ce6d9-4501-4620-bf6d-66afe2214bf1)

7. Click Preview button in right bottom side --> type "introduction" --> type "bisma"
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/2629989c-61ac-46a7-8ef7-7fb57f99298d)

## Integrate assistant with AI Agent service with custom extension

1. Download watsonx extension [here](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/blob/main/Lab%206%20-%20Increase%20productivity%20by%20enabling%20AI%20Assistant/watsonx-extension.json)

2. Hover your mouse to left section until you can see left page
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/9dfbc27b-4d84-4831-9bfb-08901c6e27c5)

3. Click Integration --> Scroll down until you can find Extensions section --> click Build cusotm extension --> set your extension name --> click Next button --> upload watsonx extension that you already downloaded --> click Next button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/e4cba98a-6e45-46a4-b9d5-65d0dbe7adff)

4. Review your extension --> click Finish button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/a7916195-a488-4db7-8b67-05e5ee8c4806)

5. Click Add link --> click Add button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/790fca56-bee2-4a0e-97bc-257ff6488739)

6. Click Next button --> set Authentication type to OAuth 2.0 --> set apikey field with your watsonx API key --> set Client authentication to Send as Body --> click Next button 
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/b4ef2c55-3db7-4489-862d-210ce9780148)

7. Review it --> click Finish button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/185dd6b3-0239-47a0-8682-3a5f02bb7484)

## Orchestrate everything

1. Go to Actions page by hovering your mouse to left pane --> Click Create action button --> type "AI Agent" --> click Save button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/b5f60090-5480-471c-ae76-40f136fbbeaf)

2. Set Assistant says with

```
Ask everything
```

3. Set Define response with Free Text
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/0a4269ec-96a4-4298-9bd3-adbd1a00d3ed)

4. Click Next step button --> click Set variable values
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/73b7cae6-be08-4c68-b4b8-19cae02fabe8)

5. Click Set new value --> select New session variable --> set Name to "ai_payload" --> set Type to Any --> click Apply button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/1a8fa5de-8ede-46d6-8dc8-5970ec0f0849)

6. Select expression --> Enlarge Expression box --> type function as below --> between "content" and "role" you type "$" until you can see dropdown --> select Action step variable and select "step 1"

```
[ {"content": , "role":"user"} ]
```

![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/c5c64817-07bb-4eb1-a3b1-e7a1351319a6)

7. Change "Continue to next step" to "Use an extension" --> set extension to "watsonx extension" --> set Operation to "AI Agent Service" --> set version to "2021-05-01" --> set ai_service_space_id to your deployed AI Agent service --> set messages to ai_payload
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/edc8ba55-0f96-4ae6-b014-9fd25243fe44)

8. Click New step button --> click Set variable value button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/6b3fe5fb-1396-415e-9056-82a3af87b4bf)

9. Click Set new variable button --> select New session variable --> set Name to "ai_response" --> set Type to Any --> click Apply button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/844fb051-64f6-4d4a-a0ed-71add1dff40c)

10. Select Expression --> Expand Expression editor --> type "$" until you see dropdown --> select watsonx extension --> select body.choices --> add "[0]["message"]["content"]" in same line --> click Apply button --> in Assistant says editor, type "$" --> type "ai_response" --> below is the output looks like
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/f3bc5247-997f-451d-8dea-88ccce358f23)

11. Click Preview button in right bottom side --> type "AI Agent" --> type "siapa presiden indonesia sekarang?"
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/af5713f3-cc16-426c-8be6-26ece69b98e8)

## Customize and deploy your assistant everywhere

1. Hover your mouse to left pane --> select Integrations --> click Open in Web Chat box
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/025dd184-72de-41a7-b469-099beafa971b)

2. Click Confirm button --> in Style tab, set Intended purpose to Carbon for AI
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/e92dad4d-a8a0-4974-9d00-63b5907e5526)

3. In Home screen tab =, ensure only "Introduction" and "AI Agent" as onversation starter
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/c4fed34f-64ed-4066-8dd6-3d1369aedd41)

4. Go to Embed tab --> copy and paste the script into your website where you want to deploy your assistant --> click Save and exit button
![image](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/38efe82e-00c9-40e4-ad49-09780b1ad788)
