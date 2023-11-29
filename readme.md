# the-sum-of-it-all

Extract summaries of your development work.

## requirements

* Github CLI - https://cli.github.com/
* JQ JSON processor - https://jqlang.github.io/jq/


## Authenticate the CLI with Github
```
> git auth login
```
https://cli.github.com/manual/gh_auth_login


## Configure the context

Global variables are set in the `context.json` and should be appropriately set depending on your usage, see `context.json.example`.


## Execute queries against the Github GraphQL API
```
> ./execute user-repos
```

Execute uses the GraphQL query stored in `user-repos.gql` to fetch all the repositories associated with the user specified in the context file and turns the list into JSON using the JQ configuration stored in `user-repos.config`. The output is sent both to the console and the file `user-repos.output`.
