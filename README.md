# static-nytimes
New York Times Cooking access point for CU Students/Faculty/Staff.

Requirements
------------
1. Javascript enabled browser.
2. CU Boulder's IdentiKey Account (This requirement is handled by the nginx web server on CU Static Server).
3. In order to be able to use the Access Code, the user must be an active
 CU Boulder Student, Faculty, or Staff.


Dependencies
------------
1. CU Static Server (cubl_static)


Installation
-------------
Place these files on the NFS drive mounted to CU Static Server. 
These files live on the mount point under {mount point}/nytimes/
(ie: /usr/local/openresty/nginx/html/static/nytimes)

CU Static Server handles the serving of these files along with authentication and permission checks.  There should be a location "/static/nytimes/activate" set in the Static Web server to proxy pass to the NYT Cooking sign-up page with the gift code.
