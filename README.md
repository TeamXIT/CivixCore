# CivixCore Civic Platform

CivixCore is an advanced civic engagement platform built with .NET Core WebAPI, Blazor WebAssembly, and MongoDB. It supports citizen issue reporting, admin dashboards, vendor job bidding/management, political constituency analytics, notifications (email, SMS, push), and geospatial issue mapping.

## Features

- **Citizen Issue Reporting**: Road, water, sanitation, etc., with photos, location, voting.
- **Admin Dashboard**: Issue management, filtering, status updates, CSV exports.
- **Vendor Module**: Marketplace for bids, assigned jobs, payment tracking, client rating.
- **Political Dashboard**: Constituency stats, top issues, resolution charts, CSV export.
- **Authentication**: JWT, role-based UI.
- **Notifications**: Email (SendGrid), Push (OneSignal), SMS (Twilio).
- **Map Visualization**: City issues mapped (OpenStreetMap/Leaflet).
- **Blazor UI**: SPA with responsive dashboards.

## Project Structure

```
CivixCore/
├── Api/
│   ├── Controllers/
│   ├── Data/
│   ├── Repositories/
│   ├── Services/
│   ├── Program.cs
│   └── appsettings.json
├── Client/
│   ├── Pages/
│   ├── Shared/
│   └── wwwroot/js/
├── Shared/
│   └── Models/
```

## Setup

1. **MongoDB**: Start a local server (`mongodb://localhost:27017`). Database name: `CivixCoreDb`.
2. **Update `appsettings.json`**: Configure SendGrid, Twilio, and OneSignal keys.
3. **Backend**: Run `dotnet run` in `Api/`.
4. **Frontend**: Run `dotnet run` in `Client/`.
5. **Visit**: Client app in browser (`https://localhost:5001` or as configured).

## API Endpoints

- `api/issues`: CRUD for issues
- `api/auth`: Login/Register
- `api/vendor`: Vendor job marketplace
- `api/political`: Political stats
- `api/report/issues/csv`: Export all issues as CSV

## Development

- .NET 7+
- MongoDB.Driver, Microsoft.AspNetCore.Authentication.JwtBearer, Blazor
- Chart.js, Leaflet.js for JS visualizations

## Contributing

Pull requests welcome! Please open issues for feature requests and bug reports.

## License

MIT
