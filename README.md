# Assignman REST API


### Main Tech Stack

- **Node**
- **Express**
- **MongoDB**

### Additional Libraries/Packages

- **@sengrid/mail** ( for sending emails )
- **jsonwebtoken**  ( authentications )
- **mongoose**      ( access mongodb from node )
- **bcrypt**        ( hashing passwords )
- **multer**        ( uploading image )
- **sharp**         ( resizing image )
- **validator**     ( validating fields )



## User API endpoints

- Create new User

| Title            	| Create new User                                                                   |
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users`                                                                     	    |
| Method           	| **POST**                                                                             	|
| Success Response 	| Code: 201 Created                                   	                            |
| Error Response   	| Code: 400 Bad Request                                                         	|

<br>

- Login User

| Title            	| Login User                                                                    	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/login`                                                                      |
| Method           	| **POST**                                                                             	|
| Success Response 	| Code: 200 OK                                                                    	|
| Error Response   	| Code: 400 Bad Request                                                         	|

<br>

- Logout User from current session

| Title            	| Logout User from current session                                                	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/logout`                                                                    	|
| Method           	| **POST**                                                                             	|
| Success Response 	| Code: 200 OK                                     	                                |
| Error Response   	| Code: 500 Internal Server Error                	                                |

<br>

- Logout User from all the sessions

| Title            	| Logout User from all the sessions                                               	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/logoutAll`                                                                	|
| Method           	| **POST**                                                                             	|
| Success Response 	| Code: 200 OK                                                                     	|
| Error Response   	| Code: 500 Internal Server Error                                               	|

<br>

- Get Current User 

| Title            	| Get Current User                                                                 	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/me`                                                                     	|
| Method           	| **GET**                                                                             	|

<br>

- Update User details   

| Title            	| Update User details                                                              	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/me`                                                                      	|
| Method           	| **PATCH**                                                                            	|
| Success Response 	| Code: 200 OK                                                                      |
| Error Response   	| Code: 400 Bad Request                                                             |

<br>

- Remove User 

| Title            	| Remove User                                                                      	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/me`                                                                      	|
| Method           	| **DELETE**                                                                           	|
| Success Response 	| Code: 200 OK                                     	                                |
| Error Response   	| Code: 500 Internal Server Error                                                 	|


<br>

- Add User Avatar

| Title            	| Add User Avatar                                                               	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/me/avatar`                                                               	|
| Method           	| **POST**                                                                             	|
| Success Response 	| Code: 200 OK                                                                    	|
| Error Response   	| Code: 400 Bad Request                                                          	|


<br>

- Delete User Avatar

| Title            	| Delete User Avatar                                                               	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/me/avatar`                                                                 	|
| Method           	| **DELETE**                                                                           	|
| Success Response 	| Code: 200 OK                                                                  	|


<br>

- Get Avatar for given User  

| Title            	| Get Avatar for given User                                                        	|
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/users/:id/avatar`                                                                	|
| Method           	| **POST**                                                                             	|
| URL Parameters    | <br>Required:<br><br>id=[Integer]<br>                                            	|
| Success Response 	| Code: 200 OK                                                                  	|
| Error Response   	| Code: 404 Not Found                                                            	|


## Task API endpoints

- Create New Task  

| Title            	|  Create New Task                                              	                |
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/tasks`                                                                 	        |
| Method           	| **POST**                                                                             	|
| Success Response 	| Code: 201 Created                                                             	|
| Error Response   	| Code: 400 Bad Request                                       	                    |


<br>

- Get all Tasks

| Title            	| Get all Tasks                                               	                    |
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/tasks`                                                                 	        |
| Method           	| **GET**                                                                           	|
| URL Parameters    | <br>completed=[Boolean]<br>limit=[Integer]<br>skip=[Integer]<br>sortBy=[String] <br><br>                                                                                	              |
| Success Response 	| Code: 200 OK                           	                                        |
| Error Response   	| Code: 500 Internal Server Error                                      	            |
| Sample Request   	| <br>/tasks?completed=true<br>/tasks?limit=10&skip=20<br>/tasks?sortBy=createdAt:desc<br>                                                              	             |

<br>

- Get a given Task   

| Title            	| Get a given Task                                               	                |
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/tasks/:id`                                                                 	    |
| Method           	| **GET**                                                                             	|
| URL Parameters    | Required:<br>id=[Integer]<br>                                                     |
| Success Response 	| Code: 200 OK                                     	                                |
| Error Response   	| Code: 404 Not Found                                                              	|
| Error Response   	| Code: 500 Internal Server Error                                                 	|


<br>

- Update a given Task

| Title            	| Update a given Task                                               	            |
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/tasks/:id`                                                                 	    |
| Method           	| **PATCH**                                                                             |
| URL Parameters    | Required:<br>id=[Integer]<br>                                                    	|
| Success Response 	| Code: 200 OK                        	                                            |
| Error Response   	| Code: 404 Not Found        	                                                    |
| Error Response   	| Code: 400 Bad Request                                       	                    |


<br>

- Remove a given Task 

| Title            	| Remove a given Task                                               	            |
|------------------	|---------------------------------------------------------------------------------	|
| URL              	| `/tasks/:id`                                                                 	    |
| Method           	| **DELETE**                                                                           	|
| URL Parameters    | Required:<br>id=[Integer]<br>                                                     |
| Success Response 	| Code: 200 OK                                                                   	|
| Error Response   	| Code: 404 Not Found                                       	                    |
| Error Response   	| Code: 500 Internal Server Error                                               	|



