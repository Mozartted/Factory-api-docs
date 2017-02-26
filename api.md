## The Projects Api (Factory)
> the Ideas behind the projects Api

The Project Api is divided into two sections,

- The Projects 
- The Tasks

> note all url links operate via the structure 'api/v1/projects/....'

The routes return data in the format
```javascript
//the json response 
{
	status: "status", //success or error
	data  : {
		//all data from route would be here
    }
}

```

## The Project Api
the project api is to have the following functionality,

- adding projects
- editing/updating projects
- color coding project
- deleting projects
- Retrieve all Projects in a department
- completing projects

Each of these operates as described below.

### adding projects
The Route : "api/v1/projects/create" -verified
this creates new projects via post variables
> POST Method

- project_name
- project_description
- status
- dept_id
- image
- color

### editing/updating projects 
The Route : "api/v1/projects/{id}/update" -verified
his creates new projects via post variables
> PUT Method

- new_project_name
- new_project_status
- new_project_department (the id)
- new_project_description
- new_project_color

### color coding projects
The Route : "api/v1/projects/{project}/colorcode" -verified
his creates updates color code via post variables
> POST Method

- color

### Deleting Projects
The Route : "api/v1/projects/{project}/remove" -verified
This remove the project specified in {project}
> DELETE Method

### Retrieve all Project 
The Route :"api/v1/projects/{department}/all" -verified
This retrieves all projects in the specified {department}
> GET Method

### Retrieving Specific Project
The Route : "api/v1/projects/{id}" -verified
This retrives details about the specific project
> GET Method

## The Task Api

the task api is to have the following functionality,

- adding tasks
- editing/updating tasks
- deleting tasks
- Retrieve all tasks in a project
- Retrieve Specific Task
- Move tasks to different Project
- completing tasks

Each of these operates as described below.

### adding tasks
The Route : "api/v1/projects/{project}/tasks/create" -verified
this creates new projects via post variables
> POST Method

- task_name
- task_description
- task_team
- task_project
- task_deadline
- task_status
- task_start
- task_end
- task_lead

### editing/updating tasks 
The Route : "api/v1/projects/tasks/{task}/edit" -verified
his creates new projects via post variables
> PUT Method

- new_task_name
- new_task_status
- new_task_project (the id)
- new_task_description
- new_task_status
- new_task_end
- new_task_team

### Deleting tasks
The Route : "api/v1/projects/tasks/{task}/remove"
This remove the project specified in {task}
> DELETE Method

### Retrieve all Tasks
The Route :"api/v1/projects/{project}/tasks/all"
This retrieves all projects in the specified {project}
> GET Method

### Retrieving Specific Task
The Route : "api/v1/projects/tasks/{task}"
This retrives details about the specific task
> GET Method

### Moving Tasks to Different Project
The Route : "api/v1/tasks/{task}/move"
This moving task to a different Project
> PUT Method

- project_id

### Completing Task
The Route: "api/v1/tasks/{task}/complete"
This sets a task to completed
> PUT Method

