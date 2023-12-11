# Workbook 8: Satying Organized


### Description

Worked collaberatively, completing a todo app that allows users to check the todos of all users, create a new user, and create new todos for all users.

## Preview

![Home Page](./frontend/images/home.png)
![Todos Page](./frontend/images/todo.png)
![New Todos Page](./frontend/images/new-todo.png)
![New User Page](./frontend/images/new-user.png)

## Authors

Aviad Churaman 
Aysu Rodgers  
Jonathan Groberg  


## Code Snippets We Thought Were Interesting

Aviad:
```
    const uniqueUserIds = new Set();

    data.forEach((task) => {
      uniqueUserIds.add(Number(task.userid));
    });
```

Jonathan:
```
function statusCodeHandler(statusCode) {
  if (statusCode != 200) {
    toastUser("Username already exists");
  } else {
    window.location.href = `./todos.html?newUserSuccess=true`;
  }
}

function toastUser(msg) {
  const toastElem = document.getElementById("toast");
  const toastMsgElem = document.getElementById("toastMsg");
  const toast = bootstrap.Toast.getOrCreateInstance(toastElem); //not sure how this actually works

  toastMsgElem.innerText = msg;
  toast.show();
}
```