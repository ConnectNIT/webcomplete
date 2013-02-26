Installation
============

1. Clone the repo
-----------------

```
  git clone http://github.com/ConnectNit/webcomplete.git
```
2. Clone Submodules
-------------------

```
  cd webcomplete
  git submodule init
  git submodule update
```

3. Enter Database Details
-------------------------

```
  cd common/config/environments
  cp params-private.php.sample params-private.php // if you are developing locally
  vi params-private.php
```
Enter your database details and save it.

4. Run Deploy Script
--------------------
```
  cd ../../..
  #chmod +x runpostdeploy
  ./runpostdeploy [environment] [migrate|no-migrate]
```
  **environment** - Your Environment for which you entered the database credentials
  **migrate|no-migrate** - Database Migrations lie in `console/migrations/`. specify whether to migrate to latest or not (defaults to no-migrate)

5. Make sure permissions are fine
---------------------------------
```
  chmod 777 backend/www/assets
  chmod 777 frontend/www/assets
  chmod 777 common/data
  chmod 777 console/runtime
  chmod 777 backend/runtime
  chmod 777 frontend/runtime
```

6. Ready to go
--------------
  Application configurations are finished and open your browser and point to www folders in backend and frontend to view frontend app and backend app respectively.

Backend Login Ids
```
  Username: admin
  Password: adminpass

  Username: demo
  Password: demopass
```  

  -Fin-
