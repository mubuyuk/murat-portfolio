# Murat Portfolio

Source code for my personal portfolio site. It is a static, client-side web app built with Blazor WebAssembly and deployed to Azure Static Web Apps.

**Live site:** https://happy-bush-02efd5d03.1.azurestaticapps.net

## Tech stack

- C# / .NET 8
- Blazor WebAssembly
- Bootstrap, with custom CSS
- Azure Static Web Apps
- GitHub Actions

There is no backend or database. The site is compiled to static files and served as they are.

## Structure

- `MuratPortfolio/Pages` – routable pages: home, education, projects and one page per project
- `MuratPortfolio/Components` – reusable Razor components such as the navbar, profile, experience timeline, project list and footer
- `MuratPortfolio/wwwroot` – stylesheets, images and other static files
- `.github/workflows` – the build and deployment workflow

## Deployment

Deployment is handled by GitHub Actions:

- A push to `master` builds the app and publishes it to the production environment in Azure Static Web Apps.
- A pull request against `master` gets its own preview environment, which is removed when the pull request is closed.
