# Lerna-Lite - OIDC Publishing Example

Example of OIDC Trusted Publishing

Please be sure to always follow the latest guidance from npm directly regarding permissions etc:

https://docs.npmjs.com/trusted-publishers

Here is how the example package that gets published from this repo's GitHub Actions has been configured to use OIDC trusted publishing on npm, and successfully forbids the use of any npm tokens whatsoever:

<img width="1153" height="994" alt="image" src="https://github.com/user-attachments/assets/a78f81f7-3e1f-40de-8dad-16e2f80e90d9" />

<br>

> [!NOTE]
> This npm config could be taken even further with GitHub Environments, and that would be recommended for real-world projects.

The referenced `release.yml` is found within this repo: [.github/workflows/release.yml](.github/workflows/release.yml)

It is only intended to demonstrate the required elements like GitHub Actions `id-token: write` permission being set, it is not prescribing a specific way to invoke `lerna publish`, you are free to invoke that however you wish with whatever arguments you wish. It is the context of being published from within GitHub Actions that matters here, again please see the official documentation on `npm` linked above to learn more.

Real release from this repo, using these settings, with the associated provenance data generated: https://www.npmjs.com/package/@lerna-lite-test/oidc

### Credits

> The code provided in this repo was mostly copied from this other Lerna repo:
> https://github.com/JamesHenry/lerna-v9-oidc-publishing-example