# External-MongoDB-Certification-Practical-Exam-Bhanu-Kiran
External MongoDB Certification Practical Exam given by me ( Bhanu Kiran ) for 5th Semester , 3rd Year on 23rd November 2026 and submitted for evaluation on Github.



<!-- # External-MongoDB-Certification-Practical-Exam-Bhanu-Kiran -->
<!-- External MongoDB Certification Practical Exam given by me ( Bhanu Kiran ) for 5th Semester , 3rd Year on 23rd November 2026 and submitted for evaluation on Github. -->

###########Theory content written by me till  we received our paper
for the Replication Experiment of Lab 
# Replication is the process by which data duplicacy is created and the data on the primary server is replicated on the other secondary servers . 
#Replica sets is of the servers sharing the data on the primary Server.
#using rs.status() we check the health of teh servers , if teh health status returned is 1 then the health of the servers is alright. 

# By the use of heartbeat the servers connect to each other , for eg . if the rs.stepDown() is called and the primary server steps down then the remaining secondary servers through the process of election select the primary server to  replace the Primary Server whi8ch is stepping down . 

# In the election process the Primary server can vote for one of the servers and the secondary server can also give itself one vote. 


# Through the process of sharding we split the data among servers to decrease  the load. 
 


 # In Sharding we do Horizontal Scaling 



 ##############Scenario 1.1##############

 Requirements: Q1 Ans
 show dbs;  
 create database college; 
 show collections; 
 create collection "students"; 

 db.students.insertOne(
    {
        _id: 1,
        rollNo: 101, 
        name: "Arun", 
        dept: "CSE",
        marks:78,
        city:"Chennai"
    }
 )


 Q2. Ans 
 db.students.insertMany(
    {
        _id: 2,
        rollNo: 102, 
        name: "Karthik", 
        dept: "CSE",
        marks:62,
        city:"Chennai"
    },
     {
        _id: 3,
        rollNo: 103, 
        name: "Suresh", 
        dept: "CSE",
        marks:91,
        city:"Trichy"
    },
     {
        _id: 4,
        rollNo: 104, 
        name: "Tanya", 
        dept: "IT",
        marks:100,
        city:"Jaipur"
    },
     {
        _id: 5,
        rollNo: 105, 
        name: "Soumya", 
        dept: "CSE",
        marks:99,
        city:"HP"
    }

 )




 Q3. Ans 
 db.students.find(); 

this will find all the documents in the collection named "students"


and this -> will return all the documents data where the dept value is "CSE"


 db.students.find(
    dept:"CSE"
 ); 
 



 Q4. Ans. 

  db.students.updateMany(

     {
    
        rollNo: 103, 
    $set:{marks:100} 
     
    },
   
     {
    
        rollNo: 102, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 101, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 100, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 99, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 98, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 97, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 96, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 95, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 94, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 93, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 92, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 91, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 90, 
    $set:{marks:100} 
     
    },
      {
    
        rollNo: 89, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 88, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 87, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 86, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 85, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 84, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 83, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 82, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 81, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 80, 
    $set:{marks:100} 
     
    },
      {
    
        rollNo: 79, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 78, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 77, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 76, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 75, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 74, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 73, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 72, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 71, 
    $set:{marks:100} 
     
    },
    
     {
    
        rollNo: 70, 
    $set:{marks:100} 
     
    },  {
    
        rollNo: 69, 
    $set:{marks:100} 
     
    },
     {
    
        rollNo: 68, 
    $set:{marks:100} 
     
    }, upsert:"true"
    
  ); 





  #Q5 Ans . 
     db.students.updateMany(
        dept:"CSE", 
        $set:{
            semester:3
        }, upsert:"true"
     )


     

     #Q6 Ans.
        db.students.deleteOne(
              rollNo: 103, 
        )



        Q7. Ans.


db.students.find();  -> This will help in  finding all the remaining Students in the collection named "students"
     



############Scenario 1.2##############




#Theory -> Membership Operators 
 operators such as $in  and $nin 
 $in is used for searching for the data for the those documents in the collection which satisfy the condition in the set i.e. if those particular documents contain the the values which are present in the set then those documents will be returned.


 $nin is used to return the data for the those documents in the collection which those particular documents are not containing the the values which are present in the set then those documents will be returned.



# For Comparisions we make use of comparision operators such as $gt , $gte , $lt , $lte etc , where
$gt is used for greater than 
$gte is used for greater than or equal to 


$lt is used for lesser than 
$gte is used for lesser than or equal to 


# For Comparisions we make use of comparision operators such as $gt , $gte , $lt , $lte etc , where
$gt is used for greater than 
$gte is used for greater than or equal to 


$lt is used for lesser than 
$gte is used for lesser than or equal to 

Q1. Ans. 
create database hr; 
 show collections; 
 create collection "employees"; 
 
-> created the databse and the collection firstly and then -> 
 We may or may not write any value for the key "_id" as that would eb automatically created by MongoDB when the JSON code written by us gets converted to BSON then the _id key is automatically added .

db.employees.insertMany(
     {
        _id: 1,
        empId: 1, 
        name: "Ramya", 
        dept: "IT",
        salary:9900,
        city:"HP"
    },
      {
        _id: 2,
        empId: 2, 
        name: "bala",
        dept: "IT",
        salary:65000,
        city:"Bengaluru"
    }, 
      {
        _id: 3,
        empId: 3, 
        name: "Charan",
        dept: "IT",
        salary:58000,
        city:"Chennai"
    }, 
      {
        _id:4,
        empId: 4,
        name: "Deepa",
        dept: "Finance",
        salary:50000,
        city:"Mumbai"
    }, 
      {
        _id: 5,
        empId: 5,
        name: "Elan",
        dept: "IT",
        salary:72000,
        city:"Chennai"
    }, 
      {
        _id: 6,
        empId: 6,
        name: "Farah",
        dept: "HR",
        salary:45000,
        city:"Delhi"
    }, 
      {
        _id: 7,
        empId: 7,
        name: "Gopal",
        dept: "Finance",
        salary:61000,
        city:"Chennai
    }, 
      {
        _id: 8
        empId: 8 
        name: "Mamta",
        dept: "IT",
        salary:110000,
        city:"HP"
    } 
)
  


  Q2 Ans.

  db.employees.find(
    salary:{$gt:60000}
  )



Q3 Ans. 
  db.employees.find(
    salary:{$gte:45000, $lte:60000}
  )

  Q4. Ans. 
   db.employees.find(
    dept:{
        $in:["Finance","IT"]
    }
  )


Q5. Ans. 

  db.employees.find(
    $or{  
        $and{
    salary:{$gte:45000}, city:"Chennai"
        },
          $or  {
    salary:{$gt:70000},dept:"HR"
        },
      
    }
  )


Q6. Ans. 

  db.employees.find(
    
   city:{
        $nin  :["Chennai, "Bengaluru"]
    }
  )



Q7. Ans. 

 db.employees.find(
    
   name:{
       $regex:["A","B", "C"]
    }
  )


  Q8. Ans 
   


    db.employees.find(
    group(
name:1, 
  salary:1
    )
  

  $sort(
    salary: -1
  ) limit 4 skip 2
