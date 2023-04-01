# program-stubs


## K8s

Usage:
  k8s roll <scope> <deployment-name>
  k8s list <scope>

Options:
  -h --help     Show this screen.

Commands:
  roll <scope> <deployment-name>   Perform a rolling restart of a deployment in <scope>
  list <scope>                     List deployments in a scope

Arguments:
  <scope>         The deployment scope (dev, stage, demo, or prod)
  <deployment-name> The name of the deployment to roll (required for the 'roll' command)

Examples:
  k8s roll prod my-deployment  # Roll the 'my-deployment' deployment in the 'prod' scope
  k8s list dev                # List deployments in the 'dev' scope


## Link

Usage:
link list
link create <id> <url>
link delete <id>
link update <id> <url>

Options:
-h --help Show this screen.

Commands:
list List all known shortlinks
create <id> <url> Create a new shortlink
delete <id> Delete a shortlink (you must be the creator)
update <id> <url> Update a shortlink (you must be the creator)

Arguments:
<id> The ID of the shortlink (e.g. 'example')
<url> The URL to shorten (required for 'create' and 'update' commands)

Examples:
link list # List all known shortlinks
link create example https://www.example.com # Create a new shortlink with ID 'example'
link delete example # Delete the 'example' shortlink (must be the creator)
link update example https://www.new-example.com # Update the URL for the 'example' shortlink (must be the creator)
