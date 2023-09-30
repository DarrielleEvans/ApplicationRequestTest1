# ApplicationRequestTest1

## Purpose
This repository contains a diagram and explanation of what I observed when using the Jtester to test my application's ability to handle 1000 requests simultaneously.

## Process
### What happened during the blitz?
During the Blitz, 1000 get requests were sent to the URL Shortener Application using Jtester. The latency returned at 40.879 ms, higher than our team aims for.

## What did you do to resolve the issue?
I created a CloudFront CDN to help reduce the latency. The AWS service will store the static content of the URL Shortener Application in various edge locations. 
This will allow the static pages to load faster for users as the distance to fetch these pages will be reduced. By implementing a CDN for the URL Shortener app, the latency was reduced to 
about 9 ms with 1000 get requests.

## What was the purpose?
The Blitz aims to measure my application's ability to handle traffic surges. By running tests, I can optimize my application infrastructure to reduce the chances 
users are having a poor experience.





