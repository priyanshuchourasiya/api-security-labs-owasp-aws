# API9 – Improper Inventory Management

## Overview
Improper inventory management results from undocumented or forgotten APIs.

## Risk Impact
- Shadow APIs
- Unpatched vulnerabilities
- Compliance issues

## Exploitation (Before Fix)
Lack of centralized visibility increases API sprawl risk.

## Fix Implemented
- Centralized API management using API Gateway.
- Managed routes, stages, and authorization in one control plane.

## IAM / AppSec Perspective
Centralized inventory is critical for governance, auditing, and lifecycle
management.

## Tools Used
- AWS API Gateway

## Evidence
- Routes and stages listed in API Gateway console
