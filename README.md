This repository is for the basic understanding of graphQL CRUD operations.

#Getall users
http://localhost:3000/users

#Get user with specific ID 
{
  user(id: "23") {
    id
    firstName
    age
    company {
      id
      name
    }
  }
}

#Get all users in company with specific ID
{
  company(id:"1") {
		users {
		  id
      firstName
		}
  }
}

#Add User and output id, firstname,age
mutation {
  addUser(firstName:"Jane Doe",age:28){
    id
    firstName
    age
  }
}


#Delete user by ID
mutation {
  deleteUser(id:"RPHcuVk") { //add id here
    id
  } 
}

#Edit user
mutation {
  editUser(id:"uiVtkA5",firstName:"Reva",age:28){
    id
    firstName
    age
  }
}