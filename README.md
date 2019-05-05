# Extracts Social Client API

Welcome to the Extracts Social ([social.extracts.io](https://social.extracts.io)) API client repository.

Check out [API.md](./API.md) for the API documentation.

## Using the API

### Getting an API Key

The Extracts Social API uses Bearer Authentication. To generate an API key:

- Log into [social.extracts.io](https://social.extracts.io)
- Click on the `cog icon` on the top right of the page
- Click `Manage API Keys`
- Click `New`
- Give the API Key a name and click `Save`
- Copy the `Secret` and store it securely

### Testing Authentication

You can use the status endpoint to test authentication:

```shell
curl -X GET https://cvqtzfgnk3.execute-api.us-east-1.amazonaws.com/Production/status \
  -H 'Accept: application/json' \
  -H 'Authorization: Bearer {secret}'
```

### OpenAPI

The Extracts Social API has OpenAPI specification that you can use to generate a suitable client. You can find the specification in [social-api.yml](./social-api.yml)