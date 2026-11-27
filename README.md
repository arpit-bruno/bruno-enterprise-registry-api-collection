# Registry API check

A Bruno collection that walks through the registry API: sign in, then create, read, update, publish, read back and delete a collection, then sign out.

## Run it

1. Copy `.env.example` to `.env`.
2. In `.env`, set:
   - `REGISTRY_URL`: the address of the registry.
   - `LICENSE_TOKEN`: your licence token.
   - `MY_NAME`: a short name in lower-case letters.
3. Open this folder in Bruno.
4. Pick the environment `Registry`.
5. Run the whole collection.

Every request checks its own result. All of them should pass.

## The licence token

The registry signs you in with the licence token the Bruno app already holds. It sends the token to License Manager, and License Manager says whether it is valid. So the token has to come from the same License Manager that this registry asks.

The app keeps the token in a file called `license.json` in its own data folder.

## What it shows

| Folder | What it proves |
| --- | --- |
| 1 Start | the registry is up |
| 2 Sign in | a made-up token is refused, a real one signs in, and the registry knows who you are |
| 3 Collections | create, read, update details, publish a version, list versions, read the content back, delete |
| 4 Finish | sign out works, and after it you are refused |

If `Create` answers 409, an earlier run stopped halfway. Run `Delete` once and start again.

`.env` is ignored by git. Never commit a real token.
