# Sending POST Requests
-   You can specify the segment in url to create a new folder in firebase. That is only a firebase thing most of the restful api's have predefine endpoints.

-   like

	-   `final url = Uri.https( 'https://shop-app-5d010-default-rtdb.firebaseio.com', '/products.json');`[](<- You can specify the segment in url to create a new folder in firebase. That is only a firebase thing most of the restful api's have predefine endpoints.
    - like
    - ```dart

 ```dart 
 		  final url = Uri.https(
        'https://shop-app-5d010-default-rtdb.firebaseio.com', '/products.json');
```



- You need to have .json at the end. And it will create a database connection for that.
	- Process through this lecture:
		-   Added post request to the firebase realtime database.
		-   Learned about body in url.https.
		-   And Some Already Know JSON info.[](<- Added post request to the firebase realtime database.
- Using Json.endcode we can set data through json as maps like structure.

- Github Code Changes:
	- https://github.com/terminal-guy/Shop-App-Flutter/commit/db046035c5db70610a7a0a9226cb3fbc6422f8f5
	- Notes: https://github.com/terminal-guy/Shop-App-Flutter/commit/bee3bb41f37d56c4b441e30db327ba5460a5c8dd
	
- Theory Continuation lectures for how to use http requests [[Working with Futures]]   

	
