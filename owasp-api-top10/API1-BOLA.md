# API1 – Broken Object Level Authorization (BOLA)

## Overview
Broken Object Level Authorization occurs when APIs fail to verify whether an
authenticated user is authorized to access a specific object.

## Risk Impact
- Unauthorized data exposure
- Horizontal privilege escalation
- Regulatory and privacy violations

## Exploitation (Before Fix)
API endpoints accepted object identifiers without validating the requester’s identity,
allowing attackers to access resources belonging to other users.

## Fix Implemented
- Enforced JWT-based authentication using Amazon Cognito.
- Implemented API Gateway JWT Authorizer to ensure every request is associated
  with an authenticated identity.
- Established a foundation for backend object ownership checks using JWT claims.

## IAM / AppSec Perspective
Identity-based access control is enforced at the gateway, enabling backend services
to perform object-level authorization using trusted identity claims.

## Tools Used
- AWS API Gateway (JWT Authorizer)
- Amazon Cognito (OIDC)
- Postman

## Evidence
- Request without token → 401 Unauthorized
- Request with valid JWT → 200 OK

