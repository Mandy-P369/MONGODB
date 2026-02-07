db.employee.insertMany([
		{
		name:"Veer Singh lodhi",
		department:"Software",
		designation:"Website developer",
		salary:10000000,
		experience:"2 years",
		city:"Sagar"
		},
                {
                name:"Gargi patel",
                department:"HR",
                designation : "HR manager",
                salary:1200000,
                experience : "2 years",
                city:"Sagar"
                }])


db.employee.insertMany([
		{
		name:"Rajebdra kurmi",
		department:"Software",
		designation:"Desktop developer",
		salary:10000030,
		experience:"3 years",
		city:"Jabalpur"
		},
                {
                 name:"Aadarsh Dubey",
                 department:"HR",
                 designation : "Employee",
                 salary:1400000,
                 experience : "5 years",
                 city:"Sagar"
                 }])


db.employee.insertMany([
		{
		name:"Prachi",
		department:"UPSC",
		designation:'IAS',
		salary:56100,
		experience:"2 years",
		city:'Lalitpur'
		},
                {
		name:"aayush",
		department:"UPSC",
		designation:"IAS",
		salary:45000,
		experience:"3 years",
		city:'Lalitput
		}])


db.employee.find()

{
  _id: ObjectId('69860bdbd6d64b96d54e49be'),
  name: 'Veer Singh lodhi',
  department: 'Software',
  designation: 'Website developer',
  salary: 10000000,
  experience: '2 years',
  city: 'Sagar'
}
{
  _id: ObjectId('69860bdbd6d64b96d54e49bf'),
  name: 'Gargi patel',
  department: 'HR',
  designation: 'HR manager',
  salary: 1200000,
  experience: '2 years',
  city: 'Sagar'
}
{
  _id: ObjectId('69860c29d6d64b96d54e49c0'),
  name: 'Rajebdra kurmi',
  department: 'Software',
  designation: 'Desktop developer',
  salary: 10000030,
  experience: '3 years',
  city: 'Jabalpur'
}
{
  _id: ObjectId('69860c29d6d64b96d54e49c1'),
  name: 'Aadarsh Dubey',
  department: 'HR',
  designation: 'Employee',
  salary: 1400000,
  experience: '5 years',
  city: 'Sagar'
}
{
  _id: ObjectId('69860e62d6d64b96d54e49c2'),
  name: 'Prachi',
  department: 'UPSC',
  designation: 'IAS',
  salary: 56100,
  experience: '2 years',
  city: 'Lalitpur'
}
{
  _id: ObjectId('69860e62d6d64b96d54e49c3'),
  name: 'aayush',
  department: 'UPSC',
  designation: 'IAS',
  salary: 45000,
  experience: '3 years',
  city: 'Lalitput'
}


db.employee.findOne({department:"HR"},{name:1})

{
  _id: ObjectId('69860bdbd6d64b96d54e49bf'),
  name: 'Gargi patel'
}


db.employee.findOne({salary:{$gt:500000}},{name:1})

{
  _id: ObjectId('69860a16d6d64b96d54e49bd'),
  name: 'aayush'
}

db.employee.find({$and:[
  {salary:{$gt:40000}},{salary:{$lt:50000}}
]})

{
  _id: ObjectId('69860e62d6d64b96d54e49c3'),
  name: 'aayush',
  department: 'UPSC',
  designation: 'IAS',
  salary: 45000,
  experience: '3 years',
  city: 'Lalitput'
}

db.employee.find({
  $and:[
    {department:"HR"},
    {experience:"2 years"}
  ]
})

{
  _id: ObjectId('69860bdbd6d64b96d54e49bf'),
  name: 'Gargi patel',
  department: 'HR',
  designation: 'HR manager',
  salary: 1200000,
  experience: '2 years',
  city: 'Sagar'
}


db.employee.find({
  $or : [
    {department :"UPSC"},
    {salary :{$gt:50000,$lt:1000000}}
  ]
})

{
  _id: ObjectId('69860e62d6d64b96d54e49c2'),
  name: 'Prachi',
  department: 'UPSC',
  designation: 'IAS',
  salary: 56100,
  experience: '2 years',
  city: 'Lalitpur'
}
{
  _id: ObjectId('69860e62d6d64b96d54e49c3'),
  name: 'aayush',
  department: 'UPSC',
  designation: 'IAS',
  salary: 45000,
  experience: '3 years',
  city: 'Lalitput'
}

db.employee.find({
  $and : [
    {experience:{$gt : "2 years"}},
    {salary:{$gt:50000 }}
  ]
})

{
  _id: ObjectId('69860a16d6d64b96d54e49bd'),
  name: 'aayush',
  department: 'Data Field',
  designation: 'Analyst Engineer',
  salary: 1000000,
  experience: 'Fresher',
  city: 'Sagar'
}
{
  _id: ObjectId('69860c29d6d64b96d54e49c0'),
  name: 'Rajebdra kurmi',
  department: 'Software',
  designation: 'Desktop developer',
  salary: 10000030,
  experience: '3 years',
  city: 'Jabalpur'
}
{
  _id: ObjectId('69860c29d6d64b96d54e49c1'),
  name: 'Aadarsh Dubey',
  department: 'HR',
  designation: 'Employee',
  salary: 1400000,
  experience: '5 years',
  city: 'Sagar'
}


db.employee.find({
  $and : [
    {experience:{$gt : "1 years"}},
    {salary:{$gt:50000 }}
  ]
})

{
  _id: ObjectId('69860a16d6d64b96d54e49bd'),
  name: 'aayush',
  department: 'Data Field',
  designation: 'Analyst Engineer',
  salary: 1000000,
  experience: 'Fresher',
  city: 'Sagar'
}
{
  _id: ObjectId('69860bdbd6d64b96d54e49be'),
  name: 'Veer Singh lodhi',
  department: 'Software',
  designation: 'Website developer',
  salary: 10000000,
  experience: '2 years',
  city: 'Sagar'
}
{
  _id: ObjectId('69860bdbd6d64b96d54e49bf'),
  name: 'Gargi patel',
  department: 'HR',
  designation: 'HR manager',
  salary: 1200000,
  experience: '2 years',
  city: 'Sagar'
}
{
  _id: ObjectId('69860c29d6d64b96d54e49c0'),
  name: 'Rajebdra kurmi',
  department: 'Software',
  designation: 'Desktop developer',
  salary: 10000030,
  experience: '3 years',
  city: 'Jabalpur'
}
{
  _id: ObjectId('69860c29d6d64b96d54e49c1'),
  name: 'Aadarsh Dubey',
  department: 'HR',
  designation: 'Employee',
  salary: 1400000,
  experience: '5 years',
  city: 'Sagar'
}
{
  _id: ObjectId('69860e62d6d64b96d54e49c2'),
  name: 'Prachi',
  department: 'UPSC',
  designation: 'IAS',
  salary: 56100,
  experience: '2 years',
  city: 'Lalitpur'
}



db.employee.insertOne(
		{
 		 name:'Rahul pandey',
  		 department:"HR",
 		 designation:"Manager",
 		 salary: 120000,
 		 experience : "2 years ",
 		 city : "Mumbai"
		})


db.employee.find({$or:
  [
    {city : 'Mumbai'},
    {designation : "Manager"}
  ]})


{
  _id: ObjectId('69861528d6d64b96d54e49c4'),
  name: 'Rahul pandey',
  department: 'HR',
  designation: 'Manager',
  salary: 120000,
  experience: '2 years ',
  city: 'Mumbai'
}





