
# API3 – Broken Object Property Level Authorization (BOPLA)

## Overview
BOPLA occurs when APIs expose or allow modification of sensitive object
properties that should not be user-controllable.

## Risk Impact
- Mass assignment attacks
- Unauthorized data modification
- Sensitive data exposure

## Exploitation (Before Fix)
Client-controlled payloads could include sensitive attributes without
sufficient authorization validation.

## Fix Implemented
- Enforced authentication at the gateway to ensure only authenticated
  identities can submit requests.
- Backend services are expected to trust identity claims from JWTs
  rather than client-supplied fields.

## IAM / AppSec Perspective
Separating identity data from client input prevents privilege manipulation
and supports secure data modeling.

## Tools Used
- Amazon Cognito
- AWS API Gateway

## Evidence
- Authenticated-only access enforced via JWT authorizer
