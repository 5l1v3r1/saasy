# SaaSy
SaaSy Framework - ASPNET Core development SaaS starter kit

### Status
TravisCI Build - [![Build Status](https://travis-ci.org/agrothe/saasy.svg?branch=master)](https://travis-ci.org/agrothe/saasy)

## Development Starter
Tired of always starting from the same place, this starter project will provide a template providing:

* Multi-tenant architecture
* Localization & Globalization at all levels (Database, Service, View)
* Authentication (ASP.NET Identity)
  * Individual accounts
  * OAuth providers
  * Active Directory provider
  * 2nd Factor authentication
* Claim based authorization with granular permissions
* User management
* Tenant management

### Routing
Routing is defined as:

`https://domain.com/{locale}/{tenant code}/{area?}/{controller}/{action}/{params?}/`

So an application page action Signup on controlller Newsletter would be:

`https://domain.com/en/app/newsletter/signup`

The Identity area uses the default Razor pages and has been mapped to just the `account` controller.

For example, our login page will be

`https://domain.com/en/app/account/login`

The default base tenant is defined as "app", so if you don't wish to have a multi-tenant application you can disable the creation of new tenants and just roll with the default or modify the code to removed tenants altogether.
