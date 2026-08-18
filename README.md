# AWS VPC Peering Lab

## Overview

This project demonstrates private network connectivity between two AWS VPCs using VPC Peering.

The lab includes VPCs, subnets, route tables, Internet Gateways, EC2 instances, Security Groups, VPC Peering, and connectivity testing.

## Architecture

![AWS VPC Peering Architecture](architecture-diagram.png)

## Network Design

| Component | VPC-A | VPC-B |
|---|---|---|
| VPC CIDR | 10.0.0.0/16 | 20.0.0.0/16 |
| Subnet | 10.0.1.0/24 | 20.0.1.0/24 |
| EC2 Private IP | 10.0.1.187 | 20.0.1.100 |

## AWS Services Used

- Amazon VPC
- VPC Peering
- Amazon EC2
- Route Tables
- Internet Gateway
- Security Groups

## VPC Peering

A VPC Peering connection was created between VPC-A and VPC-B.

**Status:** Active

## Route Configuration

### VPC-A

```text
10.0.0.0/16 → local
20.0.0.0/16 → VPC Peering
0.0.0.0/0 → Internet Gateway
