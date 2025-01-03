# CODEOWNERS feature in github 
How to Create and Use a CODEOWNERS File
1.	Location of CODEOWNERS File: /. github/CODEOWNERS 
2.	Syntax: The CODEOWNERS file follows a specific syntax to assign ownership to files or directories. Each line of the file defines a path pattern and the associated users or teams.
    Users: GitHub usernames are prefixed with @.
    Teams: Teams are defined using @org/team-name, where org is the GitHub organization name and team-name is the name of the team.
    Wildcards: Patterns like * can be used to match files or directories.


For example:
# CODEOWNERS file example
# Set @user-1 as the owner for all files
* @user-1

# Assign @user-2 to all files in the docs directory
/docs/* @user-2

# Assign a team to a specific directory
/src/ @my-org/dev-users

# Assign multiple users to a specific file
/src/main.java @user-1 @user-2

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
