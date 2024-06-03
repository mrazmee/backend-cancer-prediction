# Cancer Prediction

## Features

- Prediction with image
- Import and save files from local file
- Get prediction history


## Tech

This server is built using:

- [Hapi.JS](https://hapi.dev/) - A framework of nodeJS that is used to create a server!
- [Visual Studio Code](https://code.visualstudio.com/) - awesome text editor
- [Node .js](https://nodejs.org/) - evented I/O for the backend
- [Google Cloud Firestore](https://console.cloud.google.com/projectselector2/firestore/databases?referrer=search&authuser=2&hl=en&organizationId=112315058424&supportedpurview=project) - data storage 
- [Tensorflow js](https://www.tensorflow.org/js/guide/nodejs) - for model classification


## Installation

cancer prediction requires [Node.js](https://nodejs.org/) v18+ to run.

1. Install the dependencies and devDependencies and start the server.

```sh
cd backend-cancer-prediction
npm install
```

2. Download model from [here](https://github.com/dicodingacademy/a658-machine-learning-googlecloud/releases/download/submissions/submissions-model.zip)
3. create a cloud bucket in your google cloud console with the following conditions:

| Properti | value |
| ------ | ------ |
| Name Bucket | <your own bucket name> |
| Location type | Region -> asia-southeast2 |
| Default class | Standard |
| Control access to objects | -Uncheck enforce access prevention on this bucket |
|  | -Access Control: Uniform |
| Protect object data | None |

4. upload the model you have downloaded to the bucket. Remember, make sure you upload all files, including .bin and .json.
5. opens access to the model.json object to the public. 
6. click permission and change the value by following this field:

| Properti | value |
| ------ | ------ |
| Principals | allUsers |
| Roles | Storage Admin |

7. make a firestore database and following this step:
- choose native mode
- location --> asia-southeast2(jakarta)
- and then click "create database"

8. Run the server
```sh
npm run start 
```
## Cancer Prediction Testing

Data testing [here](https://github.com/dicodingacademy/a658-machine-learning-googlecloud/releases/download/submissions/data-test-submissions.zip)
Postman collection [here](https://github.com/dicodingacademy/a658-machine-learning-googlecloud/releases/download/submission-postman/submission-mlgc.postman_collection.json)

