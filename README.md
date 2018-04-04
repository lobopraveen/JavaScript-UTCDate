# JavaScript-UTCDate

How To Convert JavaScript Local Date to UTC And UTC To Local Date

Posted here: 
https://praveenlobo.com/blog/how-to-convert-javascript-local-date-to-utc-and-utc-to-local-date


(Migrating to GitHub AS-IS)

---

var now = new Date("January 02, 2012 22:00:00 GMT+0530");  
/* now = Mon Jan 02 2012 10:30:00 GMT-0600 (CST) */

var nowUtc = new Date( now.getTime() + (now.getTimezoneOffset() * 60000));  
/* nowUtc = Mon Jan 02 2012 16:30:00 GMT-0600 (CST) */

var nowUtc = new Date(now.getUTCFullYear(), now.getUTCMonth(), now.getUTCDate(),  now.getUTCHours(), now.getUTCMinutes(), now.getUTCSeconds());  
/* nowUtc = Mon Jan 02 2012 16:30:00 GMT-0600 (CST) */

now.toUTCString()  
/* now = Mon, 02 Jan 2012 16:30:00 GMT */

now = new Date(now.toUTCString());  
/* now = Mon Jan 02 2012 10:30:00 GMT-0600 (CST) */

var millis = now.getTime() + (now.getTimezoneOffset() * 60000)  
/* millis = 1325543400000 */

now.setTime(millis - (now.getTimezoneOffset() * 60000))  
/* now = Mon Jan 02 2012 10:30:00 GMT-0600 (CST) */
