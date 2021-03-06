## Generate release notes for a Github milestone

To generate markdown release notes that comprise the list of bugs
and issues in a GitHub milestone follow these steps:

- Clone this project
- Configure the application with the following properties:
```
releasenotes.github:
    username:
    password:
    organization:
    name:
```

NOTE: When generating release notes for a public repository, the `username` and `password` properties are optional. However, specifying them ensures that you don't hit [Github's rate limit](https://developer.github.com/v3/?#rate-limiting) easily.

- Run the following commands:

```
$ ./mvnw clean install

$ java -jar target/github-release-notes-generator-0.0.1-SNAPSHOT.jar <milestone_number> <path_to_generate_file>
```

NOTE: Make sure to use the milestone number and not the milestone name. 
