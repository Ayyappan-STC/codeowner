# CODEOWNERS feature in github 
How to Create and Use a CODEOWNERS File
1.	Location of CODEOWNERS File: /. github/CODEOWNERS 
2.	Syntax: The CODEOWNERS file follows a specific syntax to assign ownership to files or directories. Each line of the file defines a path pattern and the associated users or teams.
    Users: GitHub usernames are prefixed with @.
    Teams: Teams are defined using @org/team-name, where org is the GitHub organization name and team-name is the name of the team.
    Wildcards: Patterns like * can be used to match files or directories.


3.	Matching Patterns: The CODEOWNERS file supports the following pattern types:
        - / matches from the root directory.
        - * matches any number of characters (wildcard).
  	    - ? matches exactly one character.
        - ** matches directories and subdirectories recursively.
    Example of different patterns:
        - /src/* → matches all files in the /src/ directory.
        - /src/**/*.js → matches all JavaScript files in the /src/ directory and its subdirectories.
        - /README.md → matches the README.md file in the root of the repository.

Note: The CODEOWNERS file has a hierarchical system where the most specific pattern takes priority over more general patterns. For instance, /src/main.py will take precedence over /src/*.


Why do we need this?
1. To Ensure that the appropriate people are notified about changes to the codebase.
2. To Enforce code review policies to maintain code quality and security.
3. Streamline the review process and making it more efficient.

