# AWS VPC Peering Lab

## Overview

This project demonstrates how to establish private network connectivity between two Amazon VPCs using VPC Peering.

The lab includes two VPCs with non-overlapping CIDR ranges, public subnets, route tables, Internet Gateways, EC2 instances, security groups, and a VPC Peering connection.

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

## Configuration

### VPC-A

CIDR:

`10.0.0.0/16`

Subnet:

`10.0.1.0/24`

### VPC-B

CIDR:

`20.0.0.0/16`

Subnet:

`20.0.1.0/24`

## VPC Peering

A VPC Peering connection was created between VPC-A and VPC-B.

Peering status:

`Active`

## Route Configuration

### VPC-A Route Table

```text
10.0.0.0/16 → local
20.0.0.0/16 → VPC Peering
0.0.0.0/0   → Internet Gateway