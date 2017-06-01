# Goal
- Try AWS JavaScript SDK
- Try DynamoDB in AWS
- Sample codes are included

# Setup Tips
- [Download and unpack a local AWS DynamoDB ](http://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DynamoDBLocal.html)
- [Node.js and DynamoDB tutorials](http://docs.aws.amazon.com/amazondynamodb/latest/gettingstartedguide/GettingStarted.NodeJs.01.html)
- [Quick way to setup credentials](http://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/loading-node-credentials-shared.html)

```
# Create a text file in your home directory
# ~/.aws/credentials
[default]
aws_access_key_id = 'dummy'
aws_secret_access_key = 'dummy'
```

Command to launch DynamoDB locally:

```sh
java -Djava.library.path=./DynamoDBLocal_lib -jar DynamoDBLocal.jar -sharedDb
```

In this example, `Asia Pacific (Singapore) Region` local DB is used

```javascript
AWS.config.update({
  region: "ap-southeast-1",
  endpoint: "http://localhost:8000"
});

var credentials = new AWS.SharedIniFileCredentials({profile: 'default'});
AWS.config.credentials = credentials;
```

How to run the examples?

```sh
node MoviesCreateTable.js
node MoviesLoadData.js
node MoviesItemOps01.js
node MoviesItemOps02.js
node MoviesItemOps03.js
node MoviesItemOps04.js
node MoviesItemOps05.js
node MoviesItemOps06.js
node MoviesQuery01.js
node MoviesQuery02.js
node MoviesScan.js
node MoviesDeleteTable.js
```

# Tools
- [AWS JS SDK](http://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/installing-jssdk.html)

# References:
- [AWS SDK for JavaScript with react-native support ](https://aws.amazon.com/blogs/developer/react-native-support-in-the-aws-sdk-for-javascript/)
