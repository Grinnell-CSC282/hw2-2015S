# How to Set Environment Variables

### For Bash and Command Line:
Setting environment variables is like setting variables in other languages.
`devEnvironment="leland"`
Don't know the difference between command line and bash so thats it for 
setting...
Also make sure you `export` your variables to make them environment variables
instead of lowly shell variables.

# How to Get Environment Variables
### For Bash and Command Line:
Call them with the syntax `$devEnvironment`
so for example
`echo $devEnvironment`
would print to stdout
`leland`

### For C:
use the `getenv(const char *name)` command which return environment variables
with name 
