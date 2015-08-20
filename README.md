
# Common Standards to follow in the Web Projects

Below are the project standards we finalized to follow in all of our projects. This list will be enriched as and when a new item is discussed and adopted.

* Make sure all master data should be cached either using memcache or phpredis.

When we use third party integrations like API calls or links, we need to make sure that we handled the exceptions correctly. We have faced issues due to downtime of third-party APIs / sites.

* For laravel and zf2 having default caching tools, please check following links for reference.
http://laravel.com/docs/4.2/cache
http://framework.zend.com/manual/current/en/modules/zend.cache.storage.adapter.html

* During the time database integrations to the system, make sure that we does not use root user in the code. We have to create new user with specific access for the files to access the DB.

* Log each actions user/admin does in a separate table in the Database. (Using any no SQL tool is preferred, Mongo DB).

* Add BCC for all emails send from website with the email address and we should not use CC in any case. Also, keep the email addresses in a config / constant file so that it can be changed when ever needed without looking in to the code.

* All cron job details should logged with start and end time, cron status.

* Avoid Inline CSS and JS, also css and js  should be minified using Jenkins.

* Use any image re-sizing library to make sure that we send only images fit for the section and it should cached.

* Developers can be use costom library for this as per requirement(ST Image library) or can be use image intervention.
Image intervention provides image resizing and caching
http://image.intervention.io/

* Make sure that each page loads within 3 seconds time.

* All Foreign keys should be indexed and the SQL query must be optimized.



