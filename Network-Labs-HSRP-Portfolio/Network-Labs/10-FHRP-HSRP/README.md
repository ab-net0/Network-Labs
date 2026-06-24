# HSRP Gateway Redundancy Lab

## Objective
Implement HSRP to provide gateway redundancy and eliminate a single point of failure.

## Topology

ISP
 |
SW2
/  \
R1  R2
 \  /
  SW1
   |
  PC1

## IP Addressing

| Device | Interface | IP Address |
|----------|------------|-------------|
| PC1 | NIC | 192.168.10.10/24 |
| HSRP VIP | - | 192.168.10.1 |
| R1 | G0/0 | 192.168.10.2/24 |
| R2 | G0/1 | 192.168.10.3/24 |
| ISP | G0/0 | 10.0.12.1/24 |
| R1 | G0/2 | 10.0.12.2/24 |
| R2 | G0/0 | 10.0.12.3/24 |

## Technologies Used
- GNS3
- Cisco IOSv
- HSRP
- Static Routing

## Verification
Use:
show standby brief

## Results
- R1 Active
- R2 Standby
- Failover successful
- Connectivity maintained through virtual gateway
