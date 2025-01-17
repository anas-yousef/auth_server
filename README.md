# auth_server

[![style: very good analysis][very_good_analysis_badge]][very_good_analysis_link]
[![License: MIT][license_badge]][license_link]
[![Powered by Dart Frog](https://img.shields.io/endpoint?url=https://tinyurl.com/dartfrog-badge)](https://dartfrog.vgv.dev)

An example application built with dart_frog

[license_badge]: https://img.shields.io/badge/license-MIT-blue.svg
[license_link]: https://opensource.org/licenses/MIT
[very_good_analysis_badge]: https://img.shields.io/badge/style-very_good_analysis-B22C89.svg
[very_good_analysis_link]: https://pub.dev/packages/very_good_analysis

# About
A backend server built with [Dart Frog](https://dartfrog.vgv.dev/).
The repo currently handles the authentication of new and old users, using an SMS OTP. It uses [Supabase](https://supabase.com/) for the database, where we manage users using [Supabase triggers](https://supabase.com/docs/guides/auth/managing-user-data#advanced-techniques), this is an advanced technique to create users in your public tables, once a user authenticates and creates a session.
The API endpoints are built in a way where only users with an authenticated and active session can perform HTTP requests. We do this by utilizing middleware.
