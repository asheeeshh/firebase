# Connecting firebase to python.
Rep describing how to connect firebase database to your python application.

# Creating account on firebase.
-First go to the website https://firebase.google.com \
-Then you need to sign in using your Google account.\
-Click on `Go to console` on the top right corner.

# Creating your project.
![bandicam 2021-06-12 15-10-14-814](https://user-images.githubusercontent.com/68690233/121772002-6975f780-cb90-11eb-8a26-5f02d35c5f2e.jpg)\
-On the console click on `Add project`.\

![bandicam 2021-06-12 15-12-47-862](https://user-images.githubusercontent.com/68690233/121772085-ec974d80-cb90-11eb-9f17-180482862465.jpg)\
-Give your project any name.\

![bandicam 2021-06-12 15-13-09-274](https://user-images.githubusercontent.com/68690233/121772097-fb7e0000-cb90-11eb-942c-96ca0fc31029.jpg)\
-You can either keep this option on or off.\
-Click on create and your new database is ready for use.\

![bandicam 2021-06-12 15-17-51-345](https://user-images.githubusercontent.com/68690233/121772205-9f67ab80-cb91-11eb-93a9-1ff0696ce149.jpg)\
-Click on `Realtime database` then click on `Create Database`.\

![bandicam 2021-06-12 15-18-28-688](https://user-images.githubusercontent.com/68690233/121772258-ee154580-cb91-11eb-9521-b1d2cedd3ac7.jpg)\
-Click on Next.\

![bandicam 2021-06-12 15-18-53-210](https://user-images.githubusercontent.com/68690233/121772267-008f7f00-cb92-11eb-87af-b94df7d98f88.jpg)\
-Choose **Test Mode** then click on Enable.\

# Connecting database to application.
![bandicam 2021-06-12 15-25-40-089](https://user-images.githubusercontent.com/68690233/121772437-fae66900-cb92-11eb-9b05-c7faa547be35.jpg)\
-Click on settings then Project Settings.\

![bandicam 2021-06-12 15-27-26-368](https://user-images.githubusercontent.com/68690233/121772456-12bded00-cb93-11eb-82ac-1b7c6dfd004b.jpg)\
-Click on the HTML icon.\

![bandicam 2021-06-12 15-27-53-907](https://user-images.githubusercontent.com/68690233/121772473-249f9000-cb93-11eb-97ac-d8dce22d2d8b.jpg)\
-Enter your app name then click on **Register App**.\

![bandicam 2021-06-12 15-31-48-588](https://user-images.githubusercontent.com/68690233/121772512-66c8d180-cb93-11eb-9954-5cff8bd795c1.jpg)\
-Now copy the highlighted portion as shown in this image.

<h2><strong>Now open your code editor and paste the portion.</strong></h2>

```python
import pyrebase

firebaseConfig = {
    "apiKey": "AIzaSyDcLtabuhx2uzPAWtiwdaTx-9Il_XkHht4",
    "authDomain": "my-new-project-b7da1.firebaseapp.com",
    "databaseURL": "https://my-new-project-b7da1-default-rtdb.firebaseio.com",  #Python accepts dictionary keys as strings so you will have to make them string using quotes.
    "projectId": "my-new-project-b7da1",
    "storageBucket": "my-new-project-b7da1.appspot.com",
    "messagingSenderId": "136114402318",
    "appId": "1:136114402318:web:e3e327eeeba5b2a83e385f"
  }

firebase = pyrebase.initialize_app(firebaseConfig)
db = firebase.database()```

<h2><strong>So now your firebase realtime database is connected to your python application.<\strong><\h2>

