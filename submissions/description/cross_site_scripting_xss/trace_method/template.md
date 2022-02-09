# Cross-Site Scripting TRACE Method

## Overview

Cross-Site Scripting (XSS) is a type of injection attack where malicious scripts are injected into trusted websites. XSS vulnerabilities allow a malicious attacker to gain access to a user's account and carry out any actions that the user is able to perform, including accessing any of the user's data.

XSS TRACE method attack in {{application}} of {{target}} allows malicious attacker to {{action}}.

## Walkthrough & PoC

1. Log in to {{application}} at {{url}}
1. Send a cURL request to {{url}} using the TRACE header
1. Observe the cookie header sent with the request is shown in the response
1. Observe that the response containing reflected elements of the HTTP request

## Vulnerability Evidence

The screenshot below demonstrates the injected JavaScript executing at {{url}}:

{{screenshot}}

## Demonstrated Impact

XSS vulnerabilities can be escalated by an attacker who could pivot to bypassing Cross-Site Request Forgery (CSRF) protections, or perform account takeovers. This would give them the ability to perform any action that a logged in user can perform. For example, an attacker could gain full control over all of the application's functionality and data, depending on the user's level of permissions.

This XSS vulnerability could be further abused to {{action}} by using the following JavaScript payload:

```javascript
{{payload}}
```

Here is a screenshot of the full exploit taking place:

{{screenshot}}