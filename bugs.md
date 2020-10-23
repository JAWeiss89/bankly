# Bugs with Bankly API
- BUG #1: User gets authenticated even with incorrect pw. (POST 'auth/login') **fixed** 
- BUG #2: User gets authenticated even if username doesn't exist. (POST 'auth/login') **fixed**
- BUG #3: User registration is not validating value types. Accepts numbers for username or strings for phone number. (POST 'auth/registration') **deferred: would require JSON-schema-validation**
- BUG #4: No error handling when looking for user that doesn't exist. Needs to return 404. (GET 'users/:username') **fixed**
- BUG #5: All users route returns detailed info of all users instead of basic info (GET 'users/') **fixed**
- BUG #6: Cannot update user info. Shows unauthorized even if it's the same user trying to update. (PATCH '/users/:username') **fixed**
- BUG # 7: Nonadmin can update admin status through patch route. (PATCH 'users/:username') **fixed**