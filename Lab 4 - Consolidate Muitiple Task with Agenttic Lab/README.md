# Build AI Agent 

## Call online deployment

1. Open your online deployment you already created in Lab 3 --> copy public endpoint and store it somewhere
<img width="811" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/c221badd-f560-42fd-b203-b087883c2b31">

2. Download and import this [notebook​](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/blob/main/Lab%205%20-%20Consolidate%20Muitiple%20Task%20with%20Agenttic%20Lab/call-online-deployment-for%20participant.ipynb) into your project

3. Open the notebook and change the watsonx api key and online deployment url with yours
<img width="1644" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/281b61d3-6113-4d34-b4c8-233d8adcce16">

4. Try to ask any question related to Lab 3. If you don't find any error you can continue.
   
## Build AI Agent

1. Click New Asset button --> type "agent" in search field --> select "Build AI agent to automate tasks"
<img width="1590" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/f5d71a28-89db-4f4f-a832-d30bacaa5d6c">

2. Add description to your agent
<img width="1728" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/89e15d09-5d81-42c1-9db9-dbe925715a5c">
You can use this as example:

```
You are agent to help user answering their query and to do that you will execute several tools.
```

3. Add instruction to your agent
<img width="1728" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/f9934224-5364-47e2-8d37-416c93bad0a0">
You can use this as example:

```
You are a helpful assistant that uses tools to answer questions in detail.
When greeted, say "Hi, I am watsonx.ai agent. How can I help you?"
You must select tool that you think is the best to answer user query.
If you cannot find the answer just say "Sorry I don't know"
```

4. Keep Google Search as your basic tool
<img width="781" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/79bd8ba3-b9d2-456d-b36f-b3aa8463713d">

5. Click Add tool button --> swipe right Document Search
<img width="1572" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/3cb77388-f98e-4236-987c-d8415d96138a">

6. Select your vector index you already created in Lab 4 --> click Select button --> click x icon to go back to main Agent Lab page
<img width="1588" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/38f2091d-6820-4b0b-a590-9abba04b36c6">

7. Click Create custom tool button --> copy and paste function in this [notebook​](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/blob/main/Lab%205%20-%20Consolidate%20Muitiple%20Task%20with%20Agenttic%20Lab/call-online-deployment-for%20participant.ipynb) with your credentials into Python code editor in right section

8. Copy and paste this code into JSON schema in left section

```
{
    "input_prompt": {
        "title": "User Query",
        "description": "Input prompt or any query given by user",
        "type": "string"
    }
}
```

9. Add name and description to your Agent --> click Create button --> you can see sample output below.
<img width="813" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/356fc10c-a9ca-462e-ba12-70dc0b2fd801">

10. You can try the result using this sample prompt. The agent will help you to choose which tool to call.
<img width="812" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/6e7a829f-e727-4b3b-a497-83e167a45012">

<img width="806" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/969c008f-2548-464c-8354-c7ee01b30502">

<img width="802" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/a0373aab-cd04-4613-a52f-638b02f142b0">

11. Save your agent
<img width="1588" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/9413d79f-2f16-4373-ad5d-b971b2280297">

12. Deploy your agent as online deployment service
<img width="1596" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/297280c6-6f03-4697-b30c-dc2b12ce922c">
