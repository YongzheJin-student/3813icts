# 3813icts
3813ICT Assignment 1
Notice: There is a bug for my Assignment i have to create user or group first then i can delete the user and group.
For this Assignment I have used git hub to track the change of my file. The advantages in using the github to track the files is I can back up the resources to avoid some files that been made afterwards lead the whole project stay irresponsibly. After that, I can share it with my lecturer to get some suggestions from him. However once I get the suggestions from my tutors. Due to the bad skills of myself I cannot solve the conflict then the whole system not response properly. Finally, I use a new git resposity.<br>
For this assignment, there are two entities involved. They are users and groups. For the user they can login to the website and join the groups, so they need to have primary key, account and password. On the other hand, the group need to have a name and a primary key like id. There are many routes been used in this assignment. Because the routes have done the job like pass the data into the service and test the result in the service then response the result into the angular js file. Finally, the results will be showed in the html file. There are four components involved. The first one is menu it shows the navigation of the website. The second one is login page. Third one is homepage and finally is the admin page. <br>
I have use session storage to manage the global variable. In using that I can use the js file to judge whether the users have login or not and what is the role of the users. Then I can use that to show the specific admin page to them like only the superAdmin can create the group so only the superAdmin can see that.<br>
app.post('/api/auth', (req, res) => {<br>
        var uname = req.body.username;<br>
        var uemail = req.body.password;<br>
        var urole;<br>
        var userObj;<br>
Thie route used to judge whether the username and password is right or not and the uname is the account number that the users have entered, uemail is the password the users have entered. Then urole used to get data from the json file to judge the role of users. Userobj used to represent the data which been get from userdata.json.<br>
app.post('/api/reg', (req, res) => {<br>
    var isUser = 0;<br>
    var regUserObj;<br>
    var regUname = req.body.username;<br>
    var regUemail = req.body.password;<br>
    var regUrole = req.body.role;<br>
This route used to do the registration. The isUser sued to judge whether the users exist or not. regUserobj used to store the data been get from the userdata.json and judge the information/. regUname, regUname and regUrole used to get the data from the angular html component.<br>
app.post('/api/users', (req, res) => {<br>
app.post('/api/del', (req, res) => <br>
    var delUname = req.body.username;<br>
    var isUser = 0;<br>
    var delUserObj;<br>
    console.log(delUname)<br>
These two route working together it used to delete the users. delUname is the data that been get from the html component about the name the user want to delete. isUser used to judge the user exist or not and the delUserobj is the data which been get from the userdata.json and the first route used to show what is the users exist in the system.

app.post('/api/groups', (req, res) => {<br>
app.post('/api/groupreg', (req, res) => {<br>
    var isGroup = 0;<br>
    var regGroupObj;<br>
    var regGname = req.body.groupname;<br>
app.post('/api/groupdel', (req, res) => {<br>
    var delGname = req.body.groupname;<br>
    var isGroup = 0;<br>
    var delGroupObj;<br>
The second one is used to do the group registration. The isgroup used to check whether the group exist or not. regGroupObj represent the data in right structure to store in the group.json. The regGname get the data from the angular html.
The first one and the third one working together. The first one return the data into the angular project and show it in the html. The html input a data to send through /api/groupdel to do the deletion of data in the service,


