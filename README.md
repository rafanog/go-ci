### Install Dependencies and Start Server

```bash
# Install dependencies
go get -d

# Start the server
go run main.go
```

The API will be served at `http://localhost:3010`.

### Endpoints

The sample includes these endpoints:

**GET** /api/public
* An unprotected endpoint which returns a message on success. Does not require a valid JWT access token.

**GET** /api/private
* A protected endpoint which returns a message on success. Requires a valid JWT access token.

**GET** /api/private-scoped
* A protected endpoint which returns a message on success. Requires a valid JWT access token with a `scope` of `read:messages`.

### Running the Example With Docker

In order to run the example with docker you need to have `docker` installed.

You also need to set the environment variables as explained [previously](#add-your-credentials).

Execute in command line `sh exec.sh` to run the Docker in Linux, or `.\exec.ps1` to run the Docker in Windows.

### How to trigger tests

Just make a modification and the ci script will trigger the unitary tests
