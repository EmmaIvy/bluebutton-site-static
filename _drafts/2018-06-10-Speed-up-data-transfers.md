---
layout: post_with_category
title: Speed up data transfers
date:   2018-05-30} 9:19 PM -0600
categories: latest code
permalink: /blog/:title
badge: blog
ctas:
  - 
    title: Home
    link: /
  -
    title: Sign up for the Developer Sandbox
    link: https://sandbox.bluebutton.cms.gov/v1/accounts/create
---
# Would you like faster data transfers?

The Blue Button Team continues to look at performance improvements for the Blue Button 2.0 API. The 
ExplanationOfBenefit resource can involve a large amount of data being transferred. To improve performance
in this area we are introducing the ability to apply gzip compression. The following data types can be enabled
for compression:

This enables gzip compression for a few content types:

- text/html
- text/plain
- application/json
- application/json+fhir

The minimum payload size we will gzip is 1 kilobyte. 

## Compression is switched off by default

In order to see the benefit of gzip compression, the client must send the **Accept-Encoding: gzip** header as part of 
their request. Otherwise, the server will respond with the unmodified content type and encoding.

## An Opt-in enhancement
 
The change is an opt-in enhancement and will not create any backward compatibility issues. Developers can choose to
implement, or not. 

The change has been implemented in Release (Which release) that went live on (date).
