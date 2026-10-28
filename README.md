# postmaster by avacodes

Bring WhatsApp, Telegram and SMS into one workspace. Manage conversations, contacts, groups, templates and campaigns, or connect your own applications.

## Download

[Android companion](https://github.com/avacodes/postmaster/releases/tag/android-v0.3.0-dev): download **postmaster.apk** for workspace management, SMS sending and authorized Telegram accounts. Android 8.0 or later is required.

[PC sender](https://github.com/avacodes/postmaster/releases/tag/sender-v0.1.0-preview.1): portable Windows x64 and Linux x64 downloads for customer-owned Telegram and WhatsApp accounts. WhatsApp requires Docker. Follow the README inside the archive.

Both downloads are previews. Check the accompanying SHA-256 files. Keep the sender device, application, permissions, internet connection and provider session available.

## Connect your phone

1. Open your Postmaster workspace and choose **Senders and devices**.
2. Install the Android companion and scan the pairing QR code from your workspace.
3. Choose the SIM you want to use and complete the app's permission steps.

## Updates

Follow the update instructions in each release. Install compatible updates over the existing app to keep your workspace connections.

## .NET integration

The single preview SDK requires .NET 8 or later and includes its public request/response models. Create a scoped integration key in your workspace and keep it in your application's server secrets.

```sh
dotnet add package avacodes.postmaster --version 0.2.0-preview.2
```

Start with the [developer quickstart](https://postmaster.avacodes.org/docs/quickstart), [interactive API reference](https://postmaster.avacodes.org/docs/api-reference), [Postman collection](https://postmaster.avacodes.org/docs/tools), [C# recipes](https://postmaster.avacodes.org/docs/sdk-examples) or [AI guide](https://postmaster.avacodes.org/docs/ai-guide). Integration requests use `https://postmaster.avacodes.org` and bearer authentication, without browser sign-in.

Sending returns a message identifier after the request is saved. Check its later status or receive signed callbacks to track sending and delivery. Reuse the same idempotency key and payload when retrying an interrupted request; do not create a second send to check delivery.

[Postmaster website](https://postmaster.avacodes.org) · [Workspace sign in](https://postmaster-app.avacodes.org)

Accounts and subscriptions are currently managed by the Postmaster team. There is no public registration or online checkout. Provider restrictions and carrier charges still apply. Android WhatsApp sending is not available.
