# InvoiceManagement

<sub>Documentation drafted with claude.ai</sub>

A WPF desktop app for invoicing, in progress. `MainWindow` acts as a shell that
hosts user controls, loading `LoginView` on startup.

## Running it

The login password is read from an environment variable rather than being stored
in the app. Set it before running:

    setx InvoiceManagement "your-password"

Then:

    dotnet run

Requires .NET 9 on Windows.

## Layout

- `MainWindow.xaml` - shell, hosts the active view
- `LoginView.xaml` - password entry, checked against the environment variable
- `HomeScreenView.xaml` - post-login screen, scaffolded but not yet wired up

## State

Login currently reports success or failure in a message box; swapping the shell
over to `HomeScreenView` is the next step and is stubbed out in
`MainWindow.xaml.cs`.
