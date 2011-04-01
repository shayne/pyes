===
Api
===

This section describes the REST APIs *elasticsearch* provides (mainly) using JSON. The API is exposed using :doc:`HTTP <.//guide/reference/modules/http.html>`,  :doc:`thrift <.//guide/reference/modules/thrift.html>`,  :doc:`memcached <.//guide/reference/modules/memcached.html>`.  

Options
=======

Pretty Results
--------------

When appending **?pretty=true** to any request made, the JSON returned will be pretty formatted (use it for debugging only!).


Parameters
----------

Rest parameters (when using HTTP, map to HTTP URL parameters) follow the convention of using underscore casing.


Boolean Values
--------------

All REST APIs parameters (both request parameters and JSON body) support providing boolean "false" as the values: **false**, **0** and **off**. All other values are considered "true". Note, this is not related to fields within a document indexed treated as boolean fields.


Number Values
-------------

All REST APIs support providing numbered parameters as **string** on top of supporting the native JSON number types.


Result Casing
-------------

All REST APIs accept the **case** parameter. When set to **camelCase**, all field names in the result will be returned in camel casing, otherwise, underscore casing will be used. Note, this does not apply to the source document indexed.


JSONP
-----

All REST APIs accept a **callback** parameter resulting in a `JSONP <http://en.wikipedia.org/wiki/JSONP>`_  result.

You can also use the **source** query string parameter to substitute for the body of the request.
