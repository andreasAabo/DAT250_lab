<h1> Hand-in: short report, DAT250, LAB 4 </h1>

<h4> Link to experiment</h4>

https://github.com/andreasAabo/Software-Technology-Experiment-4

---

<h3> Technical problems </h3>

I implemented everything with a simple mapping to a HashMap. Now my post, and get (getAll) function works as expected. But my functions specifying id (/todos/:id) just don’t seam to work when I am sending request from postman. The request will have (put/delete/get) and for example this url: ```http://localhost:8080/todos?id=1``` for id = 1. No matter what I tried the functions containing: /todos/:id, just would not get accessed with postman calls. I concluded this might be due to the simple mapping used to solve this task.

---

<h3>  Pending issues with this assignment  </h3>

Depending on my issue above is my code working as intended or not, I might have pending issues with this assignment.
