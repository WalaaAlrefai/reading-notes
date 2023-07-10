1. Django Models:
The purpose of Django models is to define the structure and behavior of your data models in a Django application. Models represent database tables and encapsulate data attributes and methods to interact with the underlying database. They serve as a bridge between your application's code and the database, providing an abstraction layer that simplifies database operations.

The basic structure of a Django model involves creating a Python class that inherits from the `django.db.models.Model` base class. Each attribute of the model class represents a field in the database table, such as CharField for character data, IntegerField for integers, and so on. Additionally, you can define relationships between models using ForeignKey, OneToOneField, ManyToManyField, and other field types.

Models help in creating and managing the database schema in a Django application by providing a declarative way to define the structure of the data. Django's ORM (Object-Relational Mapping) handles the mapping between the models and the database tables, automatically creating or updating the schema based on the defined models. The ORM also provides a high-level API for performing database operations, such as creating, reading, updating, and deleting records, without writing raw SQL queries.

2. Django Admin Interface:
The Django Admin interface is a powerful built-in feature that allows you to manage and interact with the data stored in your Django application's database. It provides a user-friendly interface for performing administrative tasks, such as creating, editing, and deleting records.

Key features and functionality of the Django Admin interface include:

- Automatic CRUD operations: The admin interface automatically generates forms and views for each registered model, allowing you to perform Create, Read, Update, and Delete (CRUD) operations without writing any code.
- Search and filtering: You can search for specific records and apply filters to narrow down the displayed data.
- User authentication and permissions: The admin interface integrates with Django's authentication system, allowing you to define access permissions for different user roles.
- Customization options: The admin interface can be customized to match the specific needs of your project. You can modify the appearance, define custom actions, add custom views, and override default behaviors.

To customize the Django Admin interface, you can create a subclass of the `admin.ModelAdmin` class and register it for a specific model. This subclass allows you to specify various options, such as fieldsets, list_display, list_filter, search_fields, and more, to control the display and behavior of the admin interface for that particular model.

3. Key Components and Workflow of a Django Application:
The key components of a Django application include models, views, templates, and URLs. Here's a brief outline of their interaction:

- Models: Define the structure of the data and handle database operations using the Django ORM. Models are typically defined in the `models.py` file of an app.

- Views: Control the logic and behavior of your application. Views handle incoming requests, fetch data from models or other sources, and render responses. Views are typically defined in the `views.py` file of an app.

- Templates: Provide the presentation layer of your application. Templates define the structure and layout of the HTML pages that are sent as responses. Templates can include placeholders for dynamic data that is populated by the views. Templates are typically stored in the `templates` directory of an app.

- URLs: Map URLs to specific views in your application. URL patterns are defined in the `urls.py` file of the project and apps. The URLs module determines which view should handle a particular URL and what data should be passed to that view.

The workflow of a Django application follows a request-response cycle:
1. A user makes a request to a specific URL.
2. Django's URL dispatcher matches the requested URL to a specific view based on the URL patterns.
3. The view function associated with the matched URL is called.
4. The view retrieves or manipulates data from the models or other sources.
5. The view renders a response using a template, passing any necessary data.
6. The response is sent back to the user's browser, displaying the requested page.

By following this workflow, Django applications can handle requests, retrieve and process data, and generate dynamic HTML pages to create functional web applications.