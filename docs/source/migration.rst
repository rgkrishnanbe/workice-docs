Migration
==============

.. Note:: Unlike freelancer office, Workice CRM now requires PHP >= 7.1.3 and MySQL.

Export data as JSON
^^^^^^^^^^^^^^^^^^^^^
Download the import file from `here <https://dbz0e1mkzg4d4.cloudfront.net/tools/workice-importer.zip>`__

Extract the downloaded file and upload it to your Root folder where **freelancer office** is installed.

 - Access the URL where you uploaded the above file example **http://your-freelancer-office.com/workice-importer.php**.
 - The import file will attempt to generate a JSON version of your data and create a file named **crmdata.json** in Root folder (We will require that file to import the data to Workice CRM).

.. ATTENTION:: Download the JSON file (crmdata.json) from your server and delete file **workice-importer.php** and **crmdata.json**

Import to Workice
^^^^^^^^^^^^^^^^^^^^^^^
 - Login to Workice CRM as administrator.
 - Go to **Settings** > **System Info** > **Import** > **Freelancer Office**.
 - When a pop modal appears, choose the file **crmdata.json** (that you downloaded from your server as described above).
 - Click on **Save** button to start importing data.

.. Note:: Workice will send an email to you when import data has been completed successfully

If your data does not show correctly after importing, run the command below;

.. code-block:: shell

	php artisan app:balances

This command will attempt to re-calculate your invoices, estimates etc

Need help?
^^^^^^^^^^^
You can contact us `here for help <https://desk.workice.com>`__ or send us an email to support@workice.com