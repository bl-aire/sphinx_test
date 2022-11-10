Table 1. Available scopes and their hierarchy
|                                    Scope                                    |                                                Grants permission to:                                                |
| --------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- |
| `(no_scope)`                                                                | Identify the owner of the requesting entity.                                                                        |
| `self`                                                                      | The user’s own resources _(metascope for users, resolves to (no_scope) for services)_                               |
| `inherit`                                                                   | Everything that the token-owning entity can access _(metascope for tokens)_                                         |
| `admin-ui`                                                                  | Access the admin page. Permission to take actions via the admin page granted separately.                            |
| `admin:users`                                                               | Read, write, create and delete users and their authentication state, not including their servers or tokens.         |
| &nbsp;&nbsp;&nbsp;`admin:auth_state`                                        | Read a user’s authentication state.                                                                                 |
| &nbsp;&nbsp;&nbsp;`users`                                                   | Read and write permissions to user models (excluding servers, tokens and authentication state).                     |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users`                            | Read user models (excluding including servers, tokens and authentication state).                                    |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users:name`     | Read names of users.                                                                                                |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users:groups`   | Read users’ group membership.                                                                                       |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users:activity` | Read time of last user activity.                                                                                    |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`list:users`                            | List users, including at least their names.                                                                         |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users:name`     | Read names of users.                                                                                                |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`users:activity`                        | Update time of last user activity.                                                                                  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users:activity` | Read time of last user activity.                                                                                    |
| &nbsp;&nbsp;&nbsp;`read:roles:users`                                        | Read user role assignments.                                                                                         |
| &nbsp;&nbsp;&nbsp;`delete:users`                                            | Delete users.                                                                                                       |
| `read:roles`                                                                | Read role assignments.                                                                                              |
| &nbsp;&nbsp;&nbsp;`read:roles:users`                                        | Read user role assignments.                                                                                         |
| &nbsp;&nbsp;&nbsp;`read:roles:services`                                     | Read service role assignments.                                                                                      |
| &nbsp;&nbsp;&nbsp;`read:roles:groups`                                       | Read group role assignments.                                                                                        |
| `admin:servers`                                                             | Read, start, stop, create and delete user servers and their state.                                                  |
| &nbsp;&nbsp;&nbsp;`admin:server_state`                                      | Read and write users’ server state.                                                                                 |
| &nbsp;&nbsp;&nbsp;`servers`                                                 | Start and stop user servers.                                                                                        |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:servers`                          | Read users’ names and their server models (excluding the server state).                                             |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:users:name`     | Read names of users.                                                                                                |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`delete:servers`                        | Stop and delete users' servers.                                                                                     |
| `tokens`                                                                    | Read, write, create and delete user tokens.                                                                         |
| &nbsp;&nbsp;&nbsp;`read:tokens`                                             | Read user tokens.                                                                                                   |
| `admin:groups`                                                              | Read and write group information, create and delete groups.                                                         |
| &nbsp;&nbsp;&nbsp;`groups`                                                  | Read and write group information, including adding/removing users to/from groups.                                   |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:groups`                           | Read group models.                                                                                                  |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:groups:name`    | Read group names.                                                                                                   |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`list:groups`                           | List groups, including at least their names.                                                                        |
| &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`read:groups:name`    | Read group names.                                                                                                   |
| &nbsp;&nbsp;&nbsp;`read:roles:groups`                                       | Read group role assignments.                                                                                        |
| &nbsp;&nbsp;&nbsp;`delete:groups`                                           | Delete groups.                                                                                                      |
| `list:services`                                                             | List services, including at least their names.                                                                      |
| &nbsp;&nbsp;&nbsp;`read:services:name`                                      | Read service names.                                                                                                 |
| `read:services`                                                             | Read service models.                                                                                                |
| &nbsp;&nbsp;&nbsp;`read:services:name`                                      | Read service names.                                                                                                 |
| `read:hub`                                                                  | Read detailed information about the Hub.                                                                            |
| `access:servers`                                                            | Access user servers via API or browser.                                                                             |
| `access:services`                                                           | Access services via API or browser.                                                                                 |
| `proxy`                                                                     | Read information about the proxy’s routing table, sync the Hub with the proxy and notify the Hub about a new proxy. |
| `shutdown`                                                                  | Shutdown the hub.                                                                                                   |
| `read:metrics`                                                              | Read prometheus metrics.                                                                                            |
