# My-subconverter

Customized [subconverter](https://github.com/tindy2013/subconverter) deployed to [okteto](https://cloud.okteto.com/)

## How to build your own subconverter server in okteto?
1. Create your own account in okteto and ensure can get API Token from okteto
2. Fork this repository
3. Create some sercets in your repository
   - CR_PAT: Create a token with the permission write:packages in the access token, and then use the value of this token to create a sercet named CR_PAT in your repo
   - OKTETO_TOKEN: Get API Token from okteto to create a sercet named OKTETO_TOKEN in your repo
   - OKTETO_NAMESPACE: Create a sercet named OKTETO_NAMESPACE in your repo, The value is which namespace you want to deployed in okteto
4. Run github action again.

**Note**：This repo use GitHub Container Registry to store image, so make sure your github account has enabling improved container support. otherwise you will get the error
```
denied: failed_precondition: Improved container support has not been enabled for 'xxx'
```
To enabe the feature in github, reference the [document](https://docs.github.com/en/free-pro-team@latest/packages/getting-started-with-github-container-registry/enabling-improved-container-support#enabling-github-container-registry-for-your-personal-account)
