# git3.2Assignment
## Github Autentication

For useraccount secure purpose, certain resources are available in Github is available to be implemented. There are different modes of authentication.

-Username and password with two-factor authentication
-Personal access token
-SSH key

Authenticator implemetation methods:

-Username and password only
    * A password is created when registering an account in Github. Github recommends to use a passwod manager to generate a random and unique password. For reference, see "["Creating a strong password"] (https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-strong-password).

    * Addtional verification will be implemented whenever new and unrecognised device, for instance, a new broswer profie, a browser where the cookies have been deleted or a new computer.if the users did not set up the 2FA feature.

    *Verification code will be send to user's registered email and also notification will be appeared if using GitHub Mobile as the authentication way. 

-Two-factor authentication (2FA)
    *Time-based one time password (TOTP) application on the registered mobile device or sent as a text message to verify user's login. 

    *During chekup period of 28 days after activitation of 2FA, user can leave the check up period if successful performing 2FA is carriedout.

    *If the users cannot pass the 28th day checkup by performing 2FA, users have to reconfigure the settings before can access to the rest of the Github. 

    *WebAyth is another method of security key for the authentiaction, another choices will be using GitHub Mobile. 

-SAML single sign-on
    *This login is for the access of recources owned by an organization or enterprise account.It is authenticate though an IdP. 

-Personal Access Token
    *It is for users to use the GitHub REST API. Fine-grained personal access is available with charges. For more information, see ["Managing your personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/managing-your-personal-access-tokens)

-Authenticating with the command line: SSH
    *Upon authenticate with GitHub CLI, the CLI will find the SSH public keys on the machine and prompt out for user to select for upload. 

    *If GitHub CLI does not find the SSH public key for upload, it will generate a newSSH public/.private keypair and upload the public key to the user;s account on GitHub.com. The user then can either authenticating with a personal acess token or via web browser. For more information, see [gh auth login] (https://cli.github.com/manual/gh_auth_login)

    *User have to generate the SSH public/private keypair on the local machine and add the key into the account on GitHub.com. For more information, see ["Generating a new SSH key and adding it to the ssh-agent"](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent). 

    *Storing of key will prevent users to keep attempting the prompoted requets of entering theSSH keyphrase. For more information, see ["store the key"](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)



