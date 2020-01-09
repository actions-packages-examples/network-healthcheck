# network-healthcheck
Example for performing a network health check for the virtual environment using ping.

## Usage

* Press [`Use this template`](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).
* Open your command line interface of choice and run this script. Be sure to replace the following values:
  * `$TOKEN` with a personal access token with `public_repo` or `repo` scope
  * `$OWNER` and `$REPO` with the appropriate values.

```shell
curl -v \
  -H "Accept: application/vnd.github.everest-preview+json" \
  -H "Authorization: token $TOKEN" \
  https://api.github.com/repos/$OWNER/$REPO/dispatches \
  -X POST -d '{"event_type":"trigger"}'
```
The value of `event_type` can be any non-empty string and does not affect the build output in any way.
