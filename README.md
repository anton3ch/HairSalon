# Eau Claire's Salon

#### Tracks Eau Claire's Salon stylists and clients

#### By [Anton Ch](https://github.com/anton3ch)

## Technologies Used

- CSS
- HTML
- C#
- .NET 6.0
- ASP.Net
- Razor
- dotnet script REPL
- MySQL
- Workbench
- EF Core

## Description

Eau Claire's Salon lets owner to add and track her stylists and their clients.

## Setup/Installation Requirements

- Clone this repository to your Desktop:
  1. Your computer will need to have GIT installed. If you do not currently have GIT installed, follow [these](https://docs.github.com/en/get-started/quickstart/set-up-git) directions for installing and setting up GIT.
  2. Once GIT is installed, clone this repository by typing following commands in your command line:
     ```
     ~ $ cd Desktop
     ~/Desktop $ git clone https://github.com/anton3ch/HairSalon.git
     ~/Desktop $ cd HairSalon
     ```
- Install the [.NET 6 SDK](https://dotnet.microsoft.com/en-us/download/dotnet/6.0)
- Install Packages for EF Core:
  ```
  ~/Desktop/HairSalon $ dotnet add package Microsoft.EntityFrameworkCore -v 5.0.0
  ~/Desktop/HairSalon $ dotnet add package Pomelo.EntityFrameworkCore.MySql -v 5.0.0-alpha.2
  ```
- Setup Database:
  - Install [MySQL Community Server and MySQL Workbench](https://www.learnhowtoprogram.com/fidgetech-3-c-and-net/3-0-lessons-1-5-getting-started-with-c/3-0-0-04-installing-and-configuring-mysql). Remember your PASSWORD.
  - Open MySQL Workbench and access Local instance 3306 under MySQL Connections
  - Click on the "Administration Tab", and select "Data Import/Restore" from the list
  - Select "Import from Self-Contained File" and find file named "anton_ch.sql" located at Desktop/HairSalon/anton_ch.sql
  - Start Import
- Create .gitignore file:
  ```
   ~/Desktop/HairSalon/ $ touch .gitignore
   ~/Desktop/HairSalon/ $ echo "*/obj/
   */bin/
   */appsettings.json" > .gitignore"
  ```
- Create appsettings.json file:
  ```
   ~/Desktop/HairSalon $ cd HairSalon
   ~/Desktop/HairSalon/HairSalon $ touch appsettings.json
   ~/Desktop/HairSalon/HairSalon $ echo '{
      "ConnectionStrings": {
        "DefaultConnection": "Server=localhost;Port=3306;database=anton_ch;uid=root;pwd=[PASSWORD];"
      }
    }' > appsettings.json
  ```
  [PASSWORD] is your password

- Create MySQL database
  ```
    Open MySQLWorkbench, log in, and connect to your local server
    Go to the Administration tab, select Data Import/Restore
    Select Import from Self Contained File
    Select ../anton_ch.sql from the top level of the cloned repository, HairSalon.
    Select "New..." and set new schema name to anton_ch
    Select 'Start Import'
    Now you have a copy of the project database on your machine.
  ```

- Build the project:
  ```
   ~/Desktop/HairSalon/HairSalon $ dotnet build
  ```
- Run the project
  ```
   ~/Desktop/HairSalon/HairSalon $ dotnet run
  ```
- Visit [https://localhost:5001](https://localhost:5001) to try this application

## Known Bugs



## License

[ISC](https://opensource.org/licenses/ISC)

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

Copyright (c) 12/23/2022 Anton Ch