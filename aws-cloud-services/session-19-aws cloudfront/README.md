**Cloudfront**
AWS Cloudfront is service that deliver the content from central storage to various edge location 

Cloudfront called as CDN

Lets say your are using instgram 
one user uploaded video reels from Australia , US UK India etc.

Now user wants watch a same reel from india , when use want to access reel first time it will call to central storage and access.
Then any user from india accessing the same reel this content has been cached in india edge loction and now onwards it will be accessible without calling to central storage. So additioanl charges will be inccured for multple access.

Cloudfront provides
Security ,performance , reliabilty and much more.

Example scenario

Create s3 bucket and host a static website using cloudfront service.

Demo