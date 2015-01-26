## Grape authorization playground

A Rails-API application (based on [this tutorial](http://www.sitepoint.com/build-great-apis-grape/)) using grape that surrounds a single resource - Employee, whose  columns are: name and address age.

I created this app to test different authorization libraries such as [CanCan(Can)](https://github.com/CanCanCommunity/cancancan), [Pundit](elabs/pundit) and [the_role](the-teacher/the_role).

### Usage
Running
```
bundle install
rake db:migrate
rails s
```

List all employees:

```
curl http://localhost:3000/api/v1/employee_data.json
```

Create:

```
curl http://localhost:3000/api/v1/employee_data.json -d "name=Balaam.Ben.Beor;address=Moab;age=33"
```


Delete:

```
curl -X DELETE http://localhost:3000/api/v1/employee_data/<EMPLOYEE_ID>.json
```

Update:

```
curl -X PUT http://localhost:3000/api/v1/employee_data/<EMPLOYEE_ID>.json -d "address=Netanya"
```
