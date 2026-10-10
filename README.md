# E-Commerce Backend

A Django-based backend for an e-commerce website. This project provides REST API endpoints for products, categories, carts, orders, payments, authentication, and user management.

## Features

- Django and Django REST Framework
- Product and category management
- User authentication and authorization
- Shopping cart and order processing
- Payment integration
- Admin interface
- Database migrations
- Environment-based configuration
- API documentation support

## Technology Stack

- Python
- Django
- Django REST Framework
- PostgreSQL or SQLite
- Docker (optional)
- Git

## Requirements

- Python 3.10 or newer
- pip
- Virtual environment tool
- PostgreSQL (recommended for production)

## Installation

1. Clone the repository and change into the backend directory:

   ```bash
   git clone <repository-url>
   cd E-COMMERCE-BACKEND
   ```

2. Create and activate a virtual environment:

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Configure environment variables. Create a `.env` file based on the project's configuration template and provide the required database, secret key, and payment settings.

5. Apply database migrations:

   ```bash
   python manage.py migrate
   ```

6. Create an administrator account:

   ```bash
   python manage.py createsuperuser
   ```

7. Start the development server:

   ```bash
   python manage.py runserver
   ```

The API will usually be available at `http://127.0.0.1:8000/`.

## Project Structure

```text
E-COMMERCE-BACKEND/
├── manage.py
├── requirements.txt
├── .env.example
├── ecommerce/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── apps/
│   ├── accounts/
│   ├── products/
│   ├── cart/
│   ├── orders/
│   └── payments/
└── README.md
```

## Available Commands

```bash
python manage.py makemigrations
python manage.py migrate
python manage.py createsuperuser
python manage.py test
python manage.py runserver
```

## Environment Variables

Set the following values in your environment or `.env` file:

```text
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=sqlite:///db.sqlite3
```

Adjust the names and values according to the actual project configuration.

## API Development

- Use Django REST Framework views or viewsets for API endpoints.
- Add serializers and tests for each new API resource.
- Keep authentication and permissions consistent across endpoints.
- Validate request data and handle errors with clear responses.

## Testing

Run the test suite with:

```bash
python manage.py test
```

## Contributing

1. Create a feature branch.
2. Make focused changes and add tests.
3. Run the relevant tests.
4. Commit your changes with a clear message.
5. Open a pull request for review.

## License

This project is licensed under the MIT License unless another license is specified.
