# user-secrets-issue
user secrets does not work on wsl2

To reproduce this issue....

1. Clone to a WSL2 directory
2. run `dotnet user-secrets set SampleValue "user-secrets"

what should happen?
- it should set the user secret, navigating to / should display "user-secrets"

what does happen?
a folder named C:\Users\<my windows user name>\AppData\Roaming/Microsoft/UserSecrets/<guid> gets throwin in the root of the repo, at which point nothing is capable of building because of
an issue finding **/*.resx

(chaos insues)