# aws-env
Making it easier to work with multiple AWS cli profile keys and configs

Include `aws-env` in your bash profile config (~/.profile or ~/.bash_profile) by adding something like this:

```
# AWS Settings
export AWS_CREDENTIAL_FILE=~/.aws/credentials
export AWS_PROFILE=default
. ~/bin/aws-env
```

After that you can use it with: `aws-switch profile_name`

By default it will load the `AWS_PROFILE` profile at the shell initialization. Make sure you provide the correct `AWS_CREDENTIAL_FILE` that you are using (either ~/.aws/credentials or ~/.aws/config).

Other useful commands are: 
 * `aws-unset` to unset the AWS_env keys, 
 * `aws-list` to list all the available profiles defined in your `AWS_CREDENTIAL_FILE`
 * `aws-who` will show the current loaded profile.
