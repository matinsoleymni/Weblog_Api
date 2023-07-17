# This is a doc for API

## endpoint
<ul>
    <li><a href="#">https://domin/api/v1/posts</a></li>
    <li><a href="#">https://domin/api/v1/userss</a></li>
</ul>

<hr>

### Posts EndPoint Setting
<p>For Get All Posts From API: </p>
<ul>
    <li>Method : GET</li>
    <li>Parameters : Nothing ()</li>
    <li>Get Posts in Json "data"</li>
</ul>
Example :

|  id  |       image        |         title         |        description         |              body              |    status    |  created_at  |
|:----:|:------------------:|:---------------------:|:--------------------------:|:------------------------------:|:------------:|:------------:|
|  1   | ./assets/img/1.png | This is a test title  | this is a test description |      this is a test body       |    Enable    |  2023/11/24  |
<br>

id is: `Post Uniqe id` | Type is: `integer (numeric)`<br>
image is: `Post image address` | `string`<br>
title is : `Post title` | Type is : `string`<br>
description is : `Post Description` | Type is : `string`<br>
body is : `Post main text` | Type is : `string`<br>
status is: `Enable` or `Disable` (Show or not show to the user) | Type is: `Enum`<br>
created_at is : `Time of created Post` | Type is : `timestamps`<br><br>
{
Action: `Return Every Posts`
}<br><br><br>

<p>Add New Post From API: </p>
<ul>
    <li>Method : POST</li>
    <li>Parameters : json</li>
</ul>

Example:
```JSON
{
  "image" : "./assets/images/img.png",
  "title" : "this is a test title from api test for change with post method",
  "description" : "this is a test description from api test for change with post method",
  "body" : "this is a test body from api test for change with post method",
  "status" : "Enable"
}
```
parameters name is doing <br><br>
**Send this json to EndPoint `Posts` With `POST` Method**
<br><br>
{Action: `Add New Post With Your Data send`}<br><br><br>


<p>Delete Post From API: </p>
<ul>
    <li>Method : DELETE</li>
    <li>Parameters : json</li>
</ul>

Example:
```JSON
{
  "id": 1
}
```

"id" => `Post id for delete this id` | `numeric` <br><br>
**Send this json to EndPoint `Posts` With `DELETE` Method**<br><br>

{Action: `Delete Post where id send`}<br><br><br>

<hr><hr> <br>

### Users EndPoint Setting
<p>For Get All Users From API: </p>
<ul>
    <li>Method : GET</li>
    <li>Parameters : ?token=YOUR_API_TOKEN</li>
    <li>Get Posts in Json "data"</li>
</ul>
Example :

|  id  |   name   |       email       |    phone    |      password      |  created_at   |
|:----:|:--------:|:-----------------:|:-----------:|:------------------:|:-------------:|
|  1   | zmat2411 | zmat24@zmat24.top | 09032142424 |   654c5s6d4cfsdf   |  2023/11/24   |
<br>

id is : `User Uniqe id` | Type is : `intger (numeric)`<br>
name is : `Username` | `string`<br>
email is : `User Email` | Type is : `string`<br>
phone is : `User Phone number` | Type is : `string`<br>
password is : `User password` | Type is : `Hash_md5 - string`<br>
created_at is : `Time of register User` | Type is : `timestamps`<br><br>
{
Action: `Return Every Users`
}<br><br><br>

<p>Add New User From API: </p>
<ul>
    <li>Method : POST</li>
    <li>Parameters : ?token=YOUR_API_TOKEN || json</li>
</ul>

Example:
```JSON
{
  "id": "4",
  "name": "test",
  "email": "test@test@gmail.com",
  "phone": "09032142525",
  "password": "654c5s6d4cfsdf"
}
```

!! Created_at Automatically Add now time !!<br><br>
**Send this json to EndPoint `Users` With `POST` Method**
<br><br>
{Action: `Add New User With Your Data send`}<br><br><br>


<p>Delete User From API: </p>
<ul>
    <li>Method : DELETE</li>
    <li>Parameters : ?token=YOUR_API_TOKEN || json</li>
</ul>

Example:
```JSON
{
  "id": 1
}
```

"id" => `User id for delete this id` | `numeric` <br><br>
**Send this json to EndPoint `users` With `DELETE` Method**<br><br>

{Action: `Delete Post where id send`}<br><br><br>


<hr>
