# Wiki-API

## RESTful API

| HTTP Verbs | /articles | /articles/web-dev  |
| ------------- | ------------- |------------- |
| GET  | Fetch all article | Fetch the article on web-dev  |
| POST  | Create one article  |  |
| PUT |  |Updates the article on web-dev |
| PATCH |  |Update the article on web-dev  |
| DELETE | Delete all articles |Delete the article on web-dev  |
## GET
- find() all articles and sent result back
![image](https://user-images.githubusercontent.com/79159894/188518645-005e28ad-2252-4383-8670-2cc877f30fbd.png)

- findOne() add specific route to find specific article
- ex: add REST to the route
-  http://localhost:3000/articles/REST
![image](https://user-images.githubusercontent.com/79159894/188524380-9fe2619c-9462-4800-bd2d-abbe0a3bb426.png)
- ex: find web dev atricle
- urel encoding: whitepare represent %20
- http://localhost:3000/articles/Web%20dev
![image](https://user-images.githubusercontent.com/79159894/188525175-3bca87ca-e256-490d-96f8-5637835036df.png)


## POST
1. create a new constant to store new object in database
2. save() new object in database
- ex : 
- post a new article doc
- title: css
- content: Cascading Style Sheets used for style html
![image](https://user-images.githubusercontent.com/79159894/188515646-dd9940d9-fc59-4873-9792-38ab9b3c7f30.png)
![image](https://user-images.githubusercontent.com/79159894/188515708-79ed3151-b240-41c3-abfd-b6576802d22b.png)


## DELETE
 - use deleteMany() and not specificy deleted target to delete all object in database
 ![image](https://user-images.githubusercontent.com/79159894/188519227-f53e687d-10cb-44a3-8abf-71075728dbfc.png)
 - use deletOne() to delete specific document that match the title that is in the url requested by client
 - ex: delete Postman API Platform url page
 ![image](https://user-images.githubusercontent.com/79159894/188570481-06b45003-2e1b-4aca-bc73-c06d82a74020.png)
- check MongoDB compass, documet that url is Postman API Platform no longer exisit
 ![image](https://user-images.githubusercontent.com/79159894/188571429-6071c8db-f464-4cb4-8c0d-1c85d4e0072f.png)

 ## PUT
 - use update() to search matcging url parameter and replace the title and content with request body.
 - If we only update the content, title field will be empty because put request is meant to replace entire document.
```
 overwrite: true // turn off default action set for update()
```
 - ex: change page CSS's title and content with 
 - Postman
 - Postman is an API platform for building and using APIs.
 ![image](https://user-images.githubusercontent.com/79159894/188562981-ffd7cc73-58e5-475a-bb7c-2a9e7c7e0375.png)
- Css document no longer exisits.
- ![image](https://user-images.githubusercontent.com/79159894/188563236-53861bc3-6d98-4882-97e8-ba4d98f7ced9.png)
## PATCH
- use update() to search matcging url parameter and use $set to update the specific field of document
- ex:
- only update the Postman url page's title with Postman API Platform
- ![image](https://user-images.githubusercontent.com/79159894/188567726-885f7aeb-e652-4b68-bc3d-2680fa9bac80.png)
- content not change
- ![image](https://user-images.githubusercontent.com/79159894/188568351-15fb1685-b1c6-4203-a33f-e51a02902959.png)

