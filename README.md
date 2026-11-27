# Registry API check

A Bruno collection that walks through the registry API: get a licence token, sign in, create a collection, publish a version, read it back, delete it, sign out.

## Run it

1. Copy `.env.example` to `.env` and fill in the five values.
2. Open this folder in Bruno and pick the environment `Registry`.
3. Run the collection. Every request should pass.

## The five values

| Value | What it is |
| --- | --- |
| `REGISTRY_URL` | the address of the registry |
| `LICENSE_MANAGER_URL` | the License Manager that this registry asks at sign-in |
| `LICENSE_EMAIL` | your email on that License Manager |
| `LICENSE_KEY` | your licence key there |
| `MY_NAME` | a short name in lower-case letters |

If `Create` answers 409, run `Delete` once and start again.
