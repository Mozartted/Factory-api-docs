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
- completing projects

Each of these operates as described below.

### adding projects
The Route : "api/v1/projects/create"
this creates new projects via post variables
project_name,