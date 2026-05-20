# Heat Production Optimizer

Second-semester Software Engineering team project at the University of Southern Denmark.

This is a C# desktop application for heat production optimization based on a Danfoss-style district-heating brief. The system processes CSV time-series data, models production units and heat demand, calculates optimized schedules, and visualizes cost, emissions, heat production, electricity production/consumption, and profit scenarios.

This fork documents the project and clarifies my contributions. For the detailed breakdown, see [MY_CONTRIBUTIONS.md](./MY_CONTRIBUTIONS.md).

## My Role

- Implemented major backend/application logic modules for the optimization system.
- Built the CSV parser and source data handling for heat demand and electricity price data.
- Designed data models for time-series records, production units, heat grid data, and optimization results.
- Implemented Source Data Manager, Asset Manager, Result Data Manager, and Optimizer modules.
- Built optimization logic for production schedules, expenses, emissions, electricity production/consumption, and profit scenarios.
- Fixed chart/data issues, tested the system, and debugged core application behavior.
- Added xUnit tests for data loading, asset management, result handling, and optimization calculations.

## Tech Stack

- C#
- .NET 9
- Avalonia UI
- MVVM
- CsvHelper
- LiveCharts
- xUnit
- Docker

## Features

- CSV import for source data
- Heat demand and electricity price processing
- Production-unit and asset management
- Scenario-based heat production optimization
- Expense, emissions, electricity production, electricity consumption, and profit calculations
- Result data storage and CSV export
- LiveCharts-based visualization
- Unit tests for core modules

## Project Structure

```text
Services/
  SourceDataManager.cs    CSV loading and time-series parsing
  AssetManager.cs         Production units and heat grid setup
  ResultDataManager.cs    Optimized result storage, lookup, totals, and export
  Optimizer.cs            Scenario optimization logic

Models/                   Domain models and CSV maps
ViewModels/               MVVM state and UI logic
Views/                    Avalonia UI screens
SP2Tests/                 xUnit tests for core modules
Assets/                   Images and source CSV data
SavedData/                Generated optimized scenario outputs
```

## Technical Highlights

This project demonstrates backend-style application logic in a desktop application: data parsing, domain modeling, optimization algorithms, modular service design, UI integration, charting, and unit testing. It is especially relevant for full-stack, backend, C#, data-processing, and application developer roles.

## Running Locally

Requirements:

- .NET 9 SDK

Run the application:

```bash
dotnet restore
dotnet run
```

Run tests:

```bash
dotnet test
```
