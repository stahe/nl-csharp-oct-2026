# C# 14 leren met .NET 10

📖 **Lees de tutorial: [https://stahe.github.io/nl-csharp-oct-2026/](https://stahe.github.io/nl-csharp-oct-2026/)**

In deze cursus leert u de taal [C#](https://learn.microsoft.com/fr-fr/dotnet/csharp/) 14 en het platform [.NET](https://dotnet.microsoft.com) 10 **aan de hand van praktijkvoorbeelden**: meer dan tweehonderd programma's (bijna 300 C#-bestanden), regel voor regel toegelicht, met de resultaten van hun uitvoering erbij. De cursus begint bij de basis van de taal en behandelt databasetoegang, netwerkprogrammering en webservices.

Het is een herschrijving, voor C# 14 en .NET 10, van de cursus [De taal C# leren, versie 3.0, met het .NET 3.5-framework](https://stahe.github.io/nl-csharp-mai-2008/) (2008): dezelfde opzet, dezelfde voorbeelden, hetzelfde overkoepelende thema, maar met actuele code. Alle programma's compileren **zonder fouten of waarschuwingen** met de .NET 10 SDK en zijn uitgevoerd; de resultaten in de cursus zijn die van deze uitvoeringen.

| Cursus C# 3.0 (2008) | Cursus C# 14 (2026) |
|---|---|
| C# 3.0, .NET 3.5-framework, alleen Windows | C# 14, .NET 10 (LTS), Windows, Linux, macOS |
| Visual C# 2008 Express | VS Code + C# Dev Kit of Visual Studio 2026, opdracht `dotnet` |
| `.sln`-projecten en -oplossingen | toepassingen met één bestand (`dotnet run prog.cs`), `.slnx`-oplossingen |
| grafische gebruikersinterfaces met Windows Forms | hoofdstuk verwijderd (interfaces zijn tegenwoordig webgebaseerd) |
| LINQ „niet behandeld" | LINQ uitgebreid behandeld |
| `ArrayList`, `Hashtable`, `BinaryFormatter` | generieke collecties, `System.Text.Json` |
| NUnit 2.4, Spring.NET | MSTest 4, Microsoft.Extensions.DependencyInjection |
| `BackgroundWorker`, patroon `BeginXxx` / `EndXxx` | `Task`, `async` / `await`, annulering, `IAsyncEnumerable` |
| SQL Server 2005, ODBC, OLE DB | MySQL 8 (Laragon), MySqlConnector, Entity Framework Core |
| `WebClient`, `WebRequest` | asynchrone `HttpClient`, `TcpClient` / `TcpListener` |
| SOAP-webservices ASMX | REST- / JSON-webservices met ASP.NET Core Minimal API |

## Cursusoverzicht

| Hoofdstuk | Inhoud |
|---|---|
| Installatie | .NET 10 SDK, VS Code / Visual Studio 2026, de opdracht `dotnet`, toepassingen met één bestand, projecten, `.slnx`-oplossingen |
| Basis van de taal | typen, literalen, nullable typen, conversies, arrays, indexen en bereiken, operatoren (`??`, `??=`), `switch`-expressies en patroonherkenning, exceptions, enumeraties, parameteroverdracht, lokale functies, tuples |
| Klassen, structuren, interfaces | properties (`init`, `required`, het C# 14-sleutelwoord `field`), overerving, polymorfisme, operatoren, indexers, structuren, interfaces, generics, records, primaire constructors, C# 14-extensieleden, nullable referentietypen |
| Veelgebruikte .NET-klassen | strings, arrays, collecties, **LINQ**, tekst- en binaire bestanden, JSON, reguliere expressies (`[GeneratedRegex]`) |
| Gelaagde architecturen | lagen [DAO] / [business] / [UI], unittests met **MSTest**, **dependency injection** |
| Delegates, lambda's en gebeurtenissen | `Func`, `Action`, lambda-expressies, closures, gebeurtenissen, expressiebomen |
| Uitvoeringsthreads | `Thread`, synchronisatie (C# 13 `Lock`, `Monitor`, `Interlocked`…), gelijktijdige collecties, `Parallel` |
| **Asynchroon programmeren** (nieuw) | `Task`, `async` / `await`, `WhenAll`, annulering, voortgang, asynchrone streams, `Parallel.ForEachAsync`, `Channel<T>` |
| Databasetoegang met ADO.NET | MySQL, `MySqlConnector`, geparametriseerde query's en SQL-injectie, transacties, asynchrone methoden, `DbProviderFactory` |
| **Entity Framework Core** (nieuw) | model, CRUD, LINQ-naar-SQL, relaties, migraties, optimistische gelijktijdigheid, ruwe SQL, dependency injection |
| Webprogrammering | TCP/IP, IPv6, asynchrone TCP-clients en -servers, HTTP, `HttpClient`, SMTP |
| Webservices | REST / JSON met ASP.NET Core Minimal API, consoleclients, JavaScript-webclient |

## De rode draad: een inkomstenbelastingrekenmachine in 9 versies

Gedurende de hele cursus bouwen we, versie na versie, een applicatie voor het **berekenen van inkomstenbelasting**:

- **versie 1**: één enkel programma; **versie 2**: klassen en interfaces; **versie 3**: gegevens gelezen uit een tekstbestand of JSON-bestand;
- **versies 4 en 5**: een gelaagde architectuur, getest met MSTest en samengevoegd via dependency injection;
- **versies 6 en 7**: gegevens in een MySQL-database, gelezen met ADO.NET en vervolgens met Entity Framework Core;
- **versie 8**: een TCP-server voor de belastingberekening en zijn client;
- **versie 9**: een REST-webservice, zijn consoleclient en zijn webclient.

## Technologieën

C# 14 · .NET 10 · VS Code · Visual Studio 2026 · MSTest 4 · Microsoft.Extensions.DependencyInjection · System.Text.Json · MySQL 8 · MySqlConnector · Entity Framework Core 9 · Pomelo.EntityFrameworkCore.MySql · ASP.NET Core 10 · Laragon

## Vereisten

- Eerdere programmeerervaring in een willekeurige taal.
- De [.NET 10 SDK](https://dotnet.microsoft.com/download/dotnet/10.0) en een code-editor ([VS Code](https://code.visualstudio.com) met de extensie C# Dev Kit, of Visual Studio 2026); [Laragon](https://laragon.org) voor MySQL (hoofdstukken over databases). Installatie-instructies staan in de cursus.

## Auteur

Deze cursus en de bijbehorende code zijn geschreven door **Claude**, de AI van [Anthropic](https://www.anthropic.com) (oktober 2026), in opdracht van Serge Tahé, op basis van zijn C#-cursus uit 2008.

Nagelezen door: [Serge Tahé](https://stahe.github.io)
