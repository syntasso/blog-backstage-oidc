# Backstage with Keycloak and SKE

This Backstage instance is a companion app for the blog post [Kratix, Backstage, and
OIDC](kratix.io/blog/backstage-and-keycloak) posted on Kratix.io.

To run this app locally, you will need to:

- Authenticate with the SKE NPM registry
  - Check the guide in [Configuring the
    Plugins](https://docs.kratix.io/ske/integrations/backstage/plugins#local-development)
    in the SKE docs.
- Export the `KEYCLOAK_URL` environment variable with the URL of your Keycloak instance
  - It should look like this: `https://lemur-10.cloud-iam.com/auth/realms/myrealm/`
- Export the `PLATFORM_URL` environment variable with the URL of your Platform cluster
  - Run `kubectl --context kind-platofrm cluster-info` to get the URL

Once you have the above environment variables set, you can run the app locally with:

```sh
yarn install
yarn dev
```
