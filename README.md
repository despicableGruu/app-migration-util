# App Migration Utility

This Django utility simplifies the process of migrating a model from one app to another within your project. It leverages Django's ORM to efficiently manage the transfer, minimizing manual intervention and reducing the risk of data inconsistencies.


## How it Works

This tool streamlines the model transfer process by automating the following steps:

1. **Model Transfer:**  The utility handles the transfer of the model's definition from its current app to the desired destination app.
2. **Database Schema Update:** It adapts the database schema accordingly, ensuring that the model's table is linked to its new app.
3. **Data Migration:**  The utility manages the transfer of the model's existing data from the old table to the new one within the target app.


## Usage

1. **Prepare your Model and Apps:**
   - Ensure both your source and target apps are properly configured in your Django project.
   - Ensure you've copied the model definition and related files from the source to the target app. 
   - **Important:** Manually manage any external dependencies or relationships tied to your model before running this command.
2. **Execute the Command:**

   ```bash
   python manage.py migrate_model ModelName source_app destination_app
   ```

   - Replace `ModelName` with the name of the model you're migrating. 
   - Replace `source_app` and `destination_app` with the names of the source and destination apps, respectively.


## Notes 

-  This utility is best used for clean model transfers where data corruption isn't a concern.
-  It's crucial to understand the implications of this utility and properly manage any related data and dependencies before running the command.
-  Thoroughly test your application after migration to ensure it's functioning as intended. 
-  Feel free to submit feedback or bug reports to help us improve this utility!