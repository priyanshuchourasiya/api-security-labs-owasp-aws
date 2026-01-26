# API2 – Broken Authentication

## Overview
Broken Authentication vulnerabilities arise from weak credential handling,
improper token validation, or custom authentication logic.

## Risk Impact
- Account takeover
- Credential abuse
- Unauthorized API access

## Exploitation (Before Fix)
The API previously lacked strong authentication, allowing unauthenticated
requests to reach backend services.

## Fix Implemented
- Delegated authentication to Amazon Cognito User Pools.
- Implemented OAuth 2.0 Authorization Code Grant with OpenID Connect.
- Issued cryptographically signed JWT access tokens.
- Validated tokens at API Gateway using issuer and audience checks.

## IAM / AppSec Perspective
Centralized authentication using a managed IdP reduces attack surface,
supports token lifecycle management, and aligns with zero-trust principles.

## Tools Used
- Amazon Cognito
- AWS API Gateway
- Postman

## Evidence
- Successful `/oauth2/token` exchange
- API rejects invalid or missing tokens

