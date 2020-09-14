# Django-Rest-User-Onboarding (From Scratch)
*Using [Dj-Rest-Auth](https://github.com/jazzband/dj-rest-auth) and [Django-All-Auth](https://github.com/pennersr/django-allauth)*

A Django web application to search YouTube API. The web application has a search box where user can input search text and a search button to click afterwards to initiate the search. When the button is clicked and the search query is submitted then it leads the user to a page displaying the results of the search.

## How to Set up
__Note__: Make sure You have set up the requirements as stated [here](https://github.com/Semicolon-Tech/django-rest-user-onboarding/blob/master/README.md#prerequisite).

### Set up steps
1. Open your CLI (Terminal for linux users and Command prompt for windows users)
2. Navigate to your __workspace_folder__ using the `cd` command.
3. If you have Git installed simply __create a git repository and clone it__ using the type the following commands (for both windows and linux users)
```
    git clone <link_to_repository>
    cd <repository_name>
```

For example if you created a repository called __django_rest_user_onboarding__ so your commands will be as follows
```
    git clone https://github.com/Semicolon-Tech/django_rest_user_onboarding
    cd django_rest_user_onboarding
```

because my `<link to repository>` is __https://github.com/Semicolon-Tech/django_rest_user_onboarding__ and my `<repository_name>` is __django_rest_user_onboarding__. For those that don't have git pre-installed you can skip the steps above (but I astrongly advise you get git) and run the following commands.
```
    mkdir <project_folder_name>
    cd <project_folder_name>
```

For example if your `<project_folder_name>` is __django_rest_user_onboarding__ so your commands will be as follows
```
    mkdir django_rest_user_onboarding
    cd django_rest_user_onboarding
```

4. This step is optional but __advised__. Set up your __virtualenv__ and __activate__ it by running the following commands
    - #### Windows Users
    ```
    virtualenv venv
    venv\Scripts\activate
    ```

    - #### Linux Users
    ```
    virtualenv venv
    source venv/bin/activate
    ```

Once that is done your next terminal prompt will be prefixed with this __(venv)__. For example,
```
    C:\Users\christian\Desktop\project_folder_name>
```
will become 
```
    (venv) C:\Users\christian\Desktop\project_folder_name>
```

By the way, the name __venv__ can be changed to a different word/name but we will be using __venv__ in this setup instructions.

5. Upgrade your pip by typing the following command
```
    python -m pip install pip --upgrade
```

6. Install all python modules in requirements.txt file by typing the following file
```
    pip install django dj-rest-auth django-allauth
```

7. Start a (Django) project
```
    django-admin startproject <project_name> .
```

For example if my `<project_name>` is __django_rest_user_onboarding__ then my commands will be as follows
```
    django-admin startproject django_rest_user_onboarding .
```

__Note__: Don't miss the __.__(period/full stop) at the end of the command

7. Set up the models and database (using SQLite locally)
```
    python manage.py migrate
```

8. Create super user credentials
```
    python manage.py createsuperuser
```

Fill the required fields when the prompt comes up.

9. Once all packages have been successfully installed run the following command
```
    python manage.py runserver
```
it will output a url looking like this `http://127.0.0.1:8000`, visit the url to interact with the application

__Note__: you can find all the API endpoints in the [urls.py]() files. You can also visit `http://127.0.0.1:8000/admin` to see the admin dashboard.


## References
1. [Dj-Rest-Auth](https://github.com/jazzband/dj-rest-auth)
2. [Django-All-Auth](https://github.com/pennersr/django-allauth)