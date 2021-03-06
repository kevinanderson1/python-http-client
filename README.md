[![Travis Badge](https://travis-ci.org/sendgrid/python-http-client.svg?branch=master)](https://travis-ci.org/sendgrid/python-http-client) [![Code Climate](https://codeclimate.com/github/sendgrid/python-http-client/badges/gpa.svg)](https://codeclimate.com/github/sendgrid/python-http-client)

**Quickly and easily access any RESTful or RESTful-like API.**

If you are looking for the SendGrid API client library, please see [this repo](https://github.com/sendgrid/sendgrid-python).

# Announcements

All updates to this project is documented in our [CHANGELOG](https://github.com/sendgrid/python-http-client/blob/master/CHANGELOG.md).

# Installation

## Prerequisites

- Python version 2.6, 2.7, 3.4, 3.5 or 3.6

## Install Package

```bash
pip install python_http_client
```

or

```bash
easy_install python_http_client
```

# Quick Start

Here is a quick example:

`GET /your/api/{param}/call`

```python
import python_http_client
global_headers = {"Authorization": "Basic XXXXXXX"}
client = Client(host='base_url', request_headers=global_headers)
client.your.api._(param).call.get()
print response.status_code
print response.headers
print response.body
```

`POST /your/api/{param}/call` with headers, query parameters and a request body with versioning.

```python
import python_http_client
global_headers = {"Authorization": "Basic XXXXXXX"}
client = Client(host='base_url', request_headers=global_headers)
query_params={"hello":0, "world":1}
request_headers={"X-Test": "test"}
data={"some": 1, "awesome": 2, "data": 3}
response = client.your.api._(param).call.post(request_body=data,
                                              query_params=query_params,
                                              request_headers=request_headers)
print response.status_code
print response.headers
print response.body
```

# Usage

- [Example Code](https://github.com/sendgrid/python-http-client/tree/master/examples)

## Roadmap

If you are interested in the future direction of this project, please take a look at our [milestones](https://github.com/sendgrid/python-http-client/milestones). We would love to hear your feedback.

## How to Contribute

We encourage contribution to our projects, please see our [CONTRIBUTING](https://github.com/sendgrid/python-http-client/blob/master/CONTRIBUTING.md) guide for details.

Quick links:

- [Feature Request](https://github.com/sendgrid/python-http-client/blob/master/CONTRIBUTING.md#feature_request)
- [Bug Reports](https://github.com/sendgrid/python-http-client/blob/master/CONTRIBUTING.md#submit_a_bug_report)
- [Sign the CLA to Create a Pull Request](https://github.com/sendgrid/python-http-client/blob/master/CONTRIBUTING.md#cla)
- [Improvements to the Codebase](https://github.com/sendgrid/python-http-client/blob/master/CONTRIBUTING.mdimprovements_to_the_codebase)

# Thanks

We were inspired by the work done on [birdy](https://github.com/inueni/birdy) and [universalclient](https://github.com/dgreisen/universalclient).

# About

python-http-client is guided and supported by the SendGrid [Developer Experience Team](mailto:dx@sendgrid.com).

python-http-client is maintained and funded by SendGrid, Inc. The names and logos for python-http-client are trademarks of SendGrid, Inc.

![SendGrid Logo](https://uiux.s3.amazonaws.com/2016-logos/email-logo%402x.png)
