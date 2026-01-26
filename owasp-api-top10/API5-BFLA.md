# API5 – Broken Function Level Authorization (BFLA)

## Overview
BFLA occurs when APIs fail to restrict access to sensitive functions.

## Risk Impact
- Privilege escalation
- Unauthorized administrative access

## Exploitation (Before Fix)
API functions were accessible without enforcing route-level authorization.

## Fix Implemented
- Applied JWT authorization to API Gateway routes.
- Protected the `GET /hello` endpoint using a Cognito JWT Authorizer.

## IAM / AppSec Perspective
Gateway-level authorization enforces least privilege and prevents
unauthorized function invocation.

## Tools Used
- AWS API Gateway
- Amazon Cognito

## Evidence
- Route configuration with JWT authorization enabled

