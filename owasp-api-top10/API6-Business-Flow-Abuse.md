
# API6 – Unrestricted Access to Sensitive Business Flows

## Overview
Sensitive business flows can be abused if not adequately protected
against automation.

## Risk Impact
- Brute-force attacks
- Abuse of business logic
- Fraud

## Exploitation (Before Fix)
Critical endpoints were accessible without traffic controls.

## Fix Implemented
- Implemented rate limiting using API Gateway throttling.
- Authentication required before invoking protected flows.

## IAM / AppSec Perspective
Combining identity validation with rate limiting reduces automation risk
and supports defense-in-depth.

## Tools Used
- AWS API Gateway
- Amazon Cognito

## Evidence
- Throttling and authentication enforced at gateway
