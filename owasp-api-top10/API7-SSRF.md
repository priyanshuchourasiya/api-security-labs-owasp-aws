
# API7 – Server-Side Request Forgery (SSRF)

## Overview
SSRF occurs when APIs can be abused to make unauthorized internal requests.

## Risk Impact
- Internal network exposure
- Cloud metadata access
- Lateral movement

## Exploitation (Before Fix)
Direct backend access increased exposure to untrusted input.

## Fix Implemented
- Enforced API Gateway as the single entry point.
- Restricted backend access to authenticated gateway traffic only.

## IAM / AppSec Perspective
Using a gateway as a policy enforcement point isolates backend services
and limits request origin trust.

## Tools Used
- AWS API Gateway

## Evidence
- Backend reachable only through authenticated gateway
