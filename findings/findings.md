# Security Testing Findings

## 1. Authentication Testing

Testing was performed against the local OWASP Juice Shop authentication workflow.

Evidence included:
- Login request capture
- Authentication response analysis
- Controlled input testing
- Intruder response comparison

## 2. API Authorization

API requests associated with basket resources were examined.

Testing focused on:
- Authentication state
- Authorization headers
- Object identifiers
- Resource access behavior
- HTTP methods

## 3. Input Validation

Controlled input testing was performed to examine application behavior against security-sensitive input.

## 4. XSS-Oriented Testing

A controlled XSS-oriented input was tested.

The observed behavior should be interpreted according to the available evidence and should not automatically be treated as confirmed code execution.

## 5. Session Security

Token and session behavior was examined through captured authentication responses and subsequent authenticated requests.
