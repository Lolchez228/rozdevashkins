# ComfyAPI
# ComfyAPI
  to start celery =  celery -A comfyapi worker --loglevel=info
  Prerequites
  - Python3.8
   - Django
   - Redis install
   
To install dependencies for your Django project from a requirements.txt file, follow these steps:
Navigate to Your Project Directory:

cd /path/to/your/project
Activate Your Virtual Environment:
If you already have a virtual environment, activate it:


source env/bin/activate  # On Unix/macOS
.\env\Scripts\activate   # On Windows
If you don't have a virtual environment, create and activate one:


python -m venv env

source env/bin/activate  # On Unix/macOS
.\env\Scripts\activate   # On Windows
Install Dependencies:
 
 pip install -r requirements.txt


  
  how to run
  source env/bin/activate

  sample apis
  Login = {{base_url}}/api/users/login/
    {
    "username": "us@a.com",
    "password": "passaFRICA"
}
  Register = {{base_url}}/api/users/register/
  {
  "email": "us@a.com",
  "username":"africans",
  "password": "passaFRICA",
  "referral_code": "",
  "referral_link": ""
}


2 - Promo-codes generation
GET {{base_url}}//api/bonus/promo/generate/
YOU ONLY NEED authorization token

3 - Using promocodes
http://127.0.0.1:8000/api/bonus/promo/validate/

4 - Referal Link generate
http://localhost:8000/api/bonus/referral/generate/

5 - Payment
http://localhost:8000/api/payments/initiate/
{
    "amount": 100.00
}
will be validated against bonus earned

6 - Image generation
http://localhost:8000/api/image-generation/upload/
sent image1, image2 and must be authorized
7 - Get image
http://localhost:8000/api/image-generation/upload/status/2357bfcf-1b19-4a33-a077-b879305f42fa-e1


