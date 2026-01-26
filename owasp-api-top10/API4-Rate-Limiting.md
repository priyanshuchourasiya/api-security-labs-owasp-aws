
# API4 – Unrestricted Resource Consumption

## Overview
Unrestricted resource consumption allows attackers to abuse APIs by sending
excessive requests.

## Risk Impact
- Denial of Service (DoS)
- Increased cloud costs
- Service degradation

## Exploitation (Before Fix)
The API accepted unlimited requests without throttling or quotas.

## Fix Implemented
- Enabled API Gateway throttling on the `$default` stage.
- Configured rate and burst limits to control traffic volume.

## IAM / AppSec Perspective
Rate limiting is a critical availability control that protects backend
services and enforces fair usage policies.

## Tools Used
- AWS API Gateway (Throttling)

## Evidence
- Throttling configuration showing rate and burst limits
