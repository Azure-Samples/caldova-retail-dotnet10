# Caldova Retail — Storefront (eShopLite.StoreFx)

A small ASP.NET Core MVC storefront on .NET 10, backed by Entity Framework 6 and SQL Server. It lists products and stores, handles sign-in, and keeps a cart. This is the customer-facing app in the Caldova Retail modernization scenario.

## Setup

Before running the app, open [appsettings.json](src/eShopLite.StoreFx/appsettings.json) and replace the placeholder password in the `StoreDbContext` connection string with your SQL Server password.

Then run it with the .NET 10 SDK:

```powershell
dotnet run --project src/eShopLite.StoreFx
```

# 🔑 Demo logins

The lab applications ship with seeded accounts. Whenever a module tells you to sign in, these are the credentials.

## Caldova storefront

| Username | Password | Role | Notes |
| --- | --- | --- | --- |
| `alice` | `Password1!` | Admin, Manager | Has existing order history |
| `bob` | `Password1!` | Employee | Has existing order history |

Either account works for the sign-in and cart checks the labs ask you to run.

> ⚠️ These are throwaway credentials for a local sandbox, and the authentication behind them is deliberately insecure — salted SHA-1 password hashes. That is the "before" state the bootcamp migrates away from.