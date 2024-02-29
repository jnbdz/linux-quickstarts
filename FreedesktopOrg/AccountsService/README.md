# AccountsService | freedesktop.org | Linux | Quickstarts



The AccountsService and its use of directories like /var/lib/AccountsService/users for storing user-specific settings are part of the broader ecosystem of FreeDesktop.org specifications, although AccountsService itself isn't a formal FreeDesktop.org standard. FreeDesktop.org provides specifications, standards, and APIs for interoperability among different Linux distributions and desktop environments. The goal is to ensure a consistent and interoperable user experience across different systems and environments.

AccountsService is designed to improve the management of user accounts by providing a D-Bus interface for querying and manipulating user information. This approach is in line with the FreeDesktop.org philosophy of using D-Bus for inter-process communication and service management in the Linux desktop ecosystem. By centralizing user account information and making it accessible via D-Bus, AccountsService allows for a more consistent and standardized way of handling user accounts across different desktop environments.

While not a formal standard, AccountsService is widely adopted and supported by various desktop environments like GNOME, KDE, and others, making it a de facto part of the Linux desktop landscape. It enhances the user experience by providing features such as:

    Easy management and display of user avatars.
    Centralized handling of user session types and language settings.
    Improved performance for listing users, especially on systems with a large number of user accounts, compared to reading /etc/passwd directly.

In summary, while AccountsService isn't explicitly defined as a FreeDesktop.org standard, it follows the principles and objectives of FreeDesktop.org by promoting interoperability and standardization among Linux desktop environments.

## What's Inside /var/lib/AccountsService/users

Inside the /var/lib/AccountsService/users directory, you will find individual configuration files for each user account on the system that AccountsService knows about. These files are typically named after the usernames of the accounts. For example, if there is a user named john, you would find a file named john in this directory.

Exemple: 
```ini
[org.freedesktop.DisplayManager.AccountsService]
BackgroundFile='/home/jn/Pictures/montreal-canada-night-city-4k_1538068139.jpg'

[User]
Session=
Icon=/home/jn/.face
SystemAccount=false
```

> You should be able to add a setting for a specific Window Manager.

## Resources
- [AccountService | Software | wiki | freedesktop.org](https://www.freedesktop.org/wiki/Software/AccountsService/)
