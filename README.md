# AWS VPC Peering Lab

## Overview

This project demonstrates how to establish private network connectivity between two Amazon VPCs using VPC Peering.

The lab covers VPC creation, subnet configuration, route tables, Internet Gateways, EC2 instances, security groups, VPC Peering, routing, and connectivity testing.

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

## Architecture Components

### VPC-A

- CIDR: `10.0.0.0/16`
- Public Subnet: `10.0.1.0/24`
- Route Table: `RT-VPC-A-Public`
- Internet Gateway: `IGW-VPC-A`

### VPC-B

- CIDR: `20.0.0.0/16`
- Public Subnet: `20.0.1.0/24`
- Route Table: `RT-VPC-B-Public`
- Internet Gateway: `IGW-VPC-B`

## VPC Peering

A VPC Peering connection was created between VPC-A and VPC-B.

**Peering Status:** Active

The VPCs use non-overlapping CIDR ranges:

```text
VPC-A: 10.0.0.0/16
VPC-B: 20.0.0.0/16
