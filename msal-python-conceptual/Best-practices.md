# Best Practices for a robust enterprise ready application

You've seen that with MSAL Python you can quite simply acquire a token for a protected Web API. You also don't have to handle refreshing tokens yourself.

However, to build robust, enterprise ready applications, you will need to do a bit more. For instance you'll want to:

* [Handle exceptions](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-handling-exceptions?tabs=python), both when you acquire a token, but also when you call the protected Web API. In particular, if your application runs in an Azure AD tenant where the tenant admins have set [Conditional Access](https://github.com/AzureAD/microsoft-authentication-library-for-python/wiki/Conditional-Access-and-Claims-Challenges) policies to enforce Multiple Factor Authentication (MFA), you will need to handle a Claim challenge.

* You might want to enable [Logging](https://docs.microsoft.com/en-us/azure/active-directory/develop/msal-logging?tabs=python) to troubleshoot your application and help your users, while respecting their privacy and being compliant with GDPR.
