### Event Manager

Event Manager is a Frappe app to efficiently create, manage, and track events, attendees, and ticket sales, with features for CSV import, capacity management, and basic reporting.

### Installation

You can install this app using the [bench](https://github.com/frappe/bench) CLI:

```bash
cd $PATH_TO_YOUR_BENCH
bench get-app $URL_OF_THIS_REPO --branch develop
bench install-app event_manager
```

### Contributing

This app uses `pre-commit` for code formatting and linting. Please [install pre-commit](https://pre-commit.com/#installation) and enable it for this repository:

```bash
cd apps/event_manager
pre-commit install
```

Pre-commit is configured to use the following tools for checking and formatting your code:

- ruff
- eslint
- prettier
- pyupgrade

### CI

This app can use GitHub Actions for CI. The following workflows are configured:

- CI: Installs this app and runs unit tests on every push to `develop` branch.
- Linters: Runs [Frappe Semgrep Rules](https://github.com/frappe/semgrep-rules) and [pip-audit](https://pypi.org/project/pip-audit/) on every pull request.


### License

mit

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
  - [Events](#events)
  - [Attendees](#attendees)
  - [Ticket Sales](#ticket-sales)
  - [CSV Import](#csv-import)
- [Folder Structure](#folder-structure)
- [Contributing](#contributing)

## Features

- **Event Management**
  - Create, update, and delete events
  - Track event details: title, description, date, location, capacity
  - Search and filter events by title or date

- **Attendee Management**
  - Register attendees for events
  - Update attendee details
  - View list of attendees per event
  - Ensure event capacity is not exceeded

- **Ticket Sales**
  - Track tickets sold and tickets available
  - Automatically calculate remaining capacity
  - Generate reports: total tickets sold, revenue per event

- **CSV Import**
  - Upload CSV files to bulk create events
  - Fields supported: Event Title, Description, Event Date, Location, Capacity
