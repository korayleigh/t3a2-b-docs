# Meeting 11 - 03 Feb 22

## 1. Progress Update

- Koray has added all User Stories to Trello board and added component steps as checklist items
- Koray has completed Menu feature create and update processes
- Leigh has setup devise-jwt and completed login page function using jwt, existing users can login/logout
- Leigh has tightened up "not null" restrictions on the database and made other small revisions to DB and ERD.

## 2. Design

### 2.1. Backend

- Discussed requirement for validations for all model objects
- This will ensure that the #errors method of new model objects can be used in the various controllers as the indicator of a valid object.
- Validations should be added inline with the database schema.

### 2.2. Frontend

- Discussed method for handling the menu in app state.
- Agreed that the entire menu be downloaded at app load, which will mean that all subsequent menu manipulation (search/filter) is instant, as it will not involve any server requests.
- Agreed to implement a pre-flight check of the order at checkout stage in case any menu item is no longer available or detail has become stale.

## 3. Task Management and Planning

- Original target to have all MVP features complete by end of Friday may not happen
- Most of groundwork is done, with Rails setup and devise-jwt setup.
- Installing AWS S3 for image storage will be another larger hurdle.
- Due to commitments on Saturday, discussed Saturday would be a day off.

## 4. Blockers

### 4.1. Testing

- Not enough is understood about how to test rails controllers and models
- Need to research conventions on file locations and naming, and syntax for interacting with Rails objects.
- Agreed to seek advice from Jarrod.

### 4.2. Linting Errors

- In order to prevent pull requests on the backend repository failing linting checks, rubocop linting commands should be run locally before push.
- It may be possible to automate this process with git hooks.

## 5. Next Steps

- Koray will continue working on Menu CRUD and add validations for the menu_items and associated models.
- Leigh will continue working on Orders CRUD and add validations for the orders and associated models.
- Koray will begin looking at AWS S3 for image storage.
