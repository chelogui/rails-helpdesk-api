# Rails Helpdesk API

## Overview

This is a Helpdesk system API built with **Ruby on Rails 7**. It allows a company to manage customer support tickets, departments, employees, and reporting. The API includes features such as ticket creation, internal chat between employees, and the ability to generate reports by department, employee, or client.

## Features

- **Employee Management:** Create and manage employee records, assigning them to different departments.
- **Department Management:** Manage various departments (e.g., Accounting, Payroll, Admin).
- **Client Management:** Store and manage client information (e.g., Natal City Hall).
- **Ticket System:** Employees can create tickets with titles, descriptions, file attachments, and observations. Tickets are assigned to specific employees and linked to a client.
- **Reporting:** Generate reports based on departments, clients, or employees, with options to filter by day, month, or year. Reports can be exported as PDF files.
- **Dashboards:** Visualize helpdesk statistics for easy monitoring.
- **Internal Chat:** Real-time chat between employees with a historical log of conversations.
- **Manual Ticket Entry:** Employees can manually create and close tickets for phone-based customer support.

## Prerequisites

- Ruby 3.2+
- Rails 7+
- PostgreSQL (or another supported database)

## Getting Started

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/chelogui/rails-helpdesk-api.git
   cd rails-helpdesk-api
   ```

2. Install dependencies:

   ```bash
   bundle install
   ```

3. Set up the database:

   ```bash
   rails db:create
   rails db:migrate
   ```

4. Seed the database (optional):

   ```bash
   rails db:seed
   ```

5. Start the Rails server:

   ```bash
   rails server
   ```

   The API should now be running at `http://localhost:3000`.

### Environment Variables

You may need to configure environment variables for services like:

- **Database** configuration (`config/database.yml`)
- **Authentication** (if using OAuth or API keys)
- **File storage** (for handling ticket attachments)

### Testing

To run the test suite, use:

```bash
rails test
```

## API Endpoints

Below are some key API endpoints (replace `:id` with actual IDs as needed):

### Employees

- `GET /employees` – List all employees
- `POST /employees` – Create a new employee
- `PUT /employees/:id` – Update employee details
- `DELETE /employees/:id` – Delete an employee

### Tickets

- `GET /tickets` – List all tickets
- `POST /tickets` – Create a new ticket
- `PUT /tickets/:id` – Update a ticket
- `DELETE /tickets/:id` – Delete a ticket

### Clients

- `GET /clients` – List all clients
- `POST /clients` – Create a new client
- `PUT /clients/:id` – Update a client
- `DELETE /clients/:id` – Delete a client

### Departments

- `GET /departments` – List all departments
- `POST /departments` – Create a new department
- `PUT /departments/:id` – Update a department
- `DELETE /departments/:id` – Delete a department

For more detailed API documentation, refer to the [API Documentation](#) (link to your API docs if available).

## Reporting and Dashboards

- **Generate Reports** by departments, clients, or employees for a specific time period (day, month, year).
- **Export Reports** as PDFs for easy sharing and record-keeping.
- **Dashboards** provide visual statistics for real-time monitoring.

## Contributing

If you'd like to contribute to the project, feel free to open a pull request or issue on GitHub.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.