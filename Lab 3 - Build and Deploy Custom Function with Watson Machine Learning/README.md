# Build and Deploy Custom Function

## Import dataset used to project

1. Download dataset [here](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/blob/main/Lab%203%20-%20Build%20and%20Deploy%20Custom%20Function%20with%20Watson%20Machine%20Learning/Online-eCommerce.csv)
2. Open your project --> go to Asset tab --> click Import Asset button --> click Data Asset
<img width="1585" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/71b9120b-d128-486a-a28c-6ceac3a7b62b">

3. Click Browse button --> select dataset you already downloaded --> click Done button
<img width="1658" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/a1e3adbc-4214-4ecd-96b1-4db794e6cf84">

## Get COS credentials from IBM Cloud

1. Open this url https://cloud.ibm.com/login
<img width="1728" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/5ee60e0f-7c3a-452d-bec5-c0804ad8e103">

2. Click Hamburger icon --> click Resource list
<img width="256" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/87b3de96-996f-48a8-84c8-0efc82cedc58">

3. Expand Storage accordion --> select product Cloud Object Storage
<img width="1728" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/078be1b3-e542-426e-aeb5-03af125dff6c">

4. Type your project name to search exact bucket name in your IBM Cloud Object Storage --> copy bucket name into somewhere
  <img width="809" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/fa7b875b-6e35-4460-b0a9-09d178055e61">

5. Copy your COS credentials into somewhere
<img width="824" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/d823d6bd-ac2d-4d0f-b5d8-cc4b845c31dc">

6. Go to Endpoints in left section --> copy COS endpoint that is labelled with 'Public' and 'us-geo'
<img width="1728" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/034670c0-6cd8-41eb-89f3-b57d4f534c2c">

## Build and deploy custom function in Jupyter Notebook

1. Download notebook used [here](https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/blob/main/Lab%203%20-%20Build%20and%20Deploy%20Custom%20Function%20with%20Watson%20Machine%20Learning/QnA%20to%20dataframe-for%20participant.ipynb)

2. Click New Asset button --> type notebook in Search field --> select "Work with data and models in Python or R notebook"
<img width="1589" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/31545127-3b8c-4cc5-ba82-9873c539af56">

3. Select Local file in left section --> click Browse button and select notebook you already downloaded --> use default setting --> click Create button
<img width="1620" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/a7e69141-31d6-4bbc-81a9-ed054ff77c0a">

4. Fill your COS credentials in the notebook
<img width="1686" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/1bb652de-2d08-4642-be55-23c0497cb7bf">

5. Fill your watsonx credentials in the notebook
<img width="1687" alt="image" src="https://github.ibm.com/Indonesia-Client-Engineering/workshop-telkom-partnership-feb2025/assets/421171/682783cb-b143-444f-886f-38f409917f33">

6. Ask your instructor for next steps
