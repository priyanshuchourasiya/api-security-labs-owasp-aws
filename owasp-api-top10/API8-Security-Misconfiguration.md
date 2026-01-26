# API8 – Security Misconfiguration

## Overview
Security misconfiguration includes insecure defaults, exposed endpoints,
and missing protections.

## Risk Impact
- Data exposure
- Unauthorized access
- Increased attack surface

## Exploitation (Before Fix)
APIs without enforced HTTPS or centralized security controls were vulnerable.

## Fix Implemented
- Enforced HTTPS using AWS-managed API Gateway invoke URLs.
- Centralized authentication and authorization.
- Exposed only required routes.

## IAM / AppSec Perspective
Managed services with secure defaults reduce configuration drift and
human error.

## Tools Used
- AWS API Gateway
- Amazon Cognito

## Evidence
- HTTPS invoke URL
- JWT-protected routes

