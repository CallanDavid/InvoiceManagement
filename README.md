# InvoiceManagement

<sub>Documentation drafted with claude.ai</sub>

A WPF desktop app for invoicing. `MainWindow` acts as a shell and swaps user
controls into it - login first, then the home screen.

## Running it

The login password is read from an environment variable rather than being stored
in the app. Set it before running:

    setx InvoiceManagement "your-password"

Then:

    dotnet run

Requires .NET 9 on Windows.

## Layout

- `MainWindow.xaml` - shell, hosts the active view
- `LoginView.xaml` - password entry
- `HomeScreenView.xaml` - post-login screen
