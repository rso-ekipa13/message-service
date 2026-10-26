# message-service

Stores and delivers encrypted messages. The service never sees the content: it keeps MLS ciphertexts in ScyllaDB, orders group changes by epoch, lets a device catch up after being offline, and deletes messages when a disappearing timer runs out.

Every stored message is announced as an event on NATS, which is how the realtime and notification services find out about it.

Built with .NET 10 and ScyllaDB.

Owner: Amar Mehić. Status: planned.

## Where this fits

This is one of the repositories of [Pretty Good Pigeon](https://github.com/rso-ekipa13), an end-to-end encrypted messenger built by ekipa 13 for the Cloud Computing course at UL FRI (2026/27). The architecture, plan and decisions live in [docs](https://github.com/rso-ekipa13/docs).

`main` only changes through pull requests; day-to-day work goes to `dev`.
