# Day 6 - ARP

## Full Form

Address Resolution Protocol

## Purpose

Converts an IP address into a MAC address.

## Why ARP is Needed

Devices communicate using MAC addresses on local networks.

If a device only knows an IP address, ARP helps find the MAC address.

## Example

192.168.1.20
↓

ARP
↓

00-1A-2B-3C-4D-5E

## Command Practiced

arp -a

## Observation

The ARP table contains IP addresses and their corresponding MAC addresses.
