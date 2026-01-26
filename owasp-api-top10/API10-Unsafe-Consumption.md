# API10 – Unsafe Consumption of APIs

## Overview
Unsafe API consumption occurs when services trust upstream or downstream APIs
without validation.

## Risk Impact
- Supply chain compromise
- Data integrity issues
- Lateral attacks

## Exploitation (Before Fix)
Unvalidated requests could propagate to backend integrations.

## Fix Implemented
- Enforced JWT validation at API Gateway.
- Ensured only authenticated, authorized requests reach backend services.

## IAM / AppSec Perspective
This aligns with zero-trust architecture, where no request is trusted
without verification.

## Tools Used
- AWS API Gateway
- Amazon Cognito

## Evidence
- JWT authorizer attached to backend integration

