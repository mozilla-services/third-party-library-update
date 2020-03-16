## TODO

 - Go through and fix all the imports (add missing, remove unused)
 - Add copyright and license
 - Rename the github repo to 'updatebot' and update the holly job
 - Update the holly job to import automation and run
 - Get a Google Cloud account and set up a Google Cloud SQL databse
 - Create a MySQLDatabase in components/db.py
 - Retrieve the mysql database password from taskcluster secret and pass it through to the database
 - Implement ./mach vendor --check-for-update which returns nothing if the library is up to date, or the new version identifier (commit hash probably) if there is a new version
 - Fix mach_vendor.check_for_update to return the information gathered
 - Implement the database function calls in automation that don't exist
   - For Hardcoded Database, just make the save() do nothing...
 - Update run_command to catch the timeout exception and grab the output per https://stackoverflow.com/questions/60675828/
 - Fix the except block that does nothing in automation.py
 - Come up with a better naming convention that file_bug/fileBug in bugzilla.py/bugzilla_api.py
 - Attach the phabricator patch
 - Figure out how we're going to figure out who to needinfo/flag for review
 - Figure out how real python applications are made these days and make this look like them. Something about requirements.txt?
 - Add a description of the project in this file
 - Handle if ./mach vendor fails, and then save the job with a note about merge conflicts, and file a bug
 - Create process_existing_job
   - Going to need to read the failed jobs off taskcluster
   - Handle if the build job failed
   - Handle if tests failed
   - File comments on the bug and place a needinfo
   - If stuff succeeded flag the patch for review