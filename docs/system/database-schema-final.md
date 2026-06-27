# WuMama Database Schema Final Direction

Version: v0.6

## Purpose

Define the database direction before WuMama-System development.

## Core Tables

users
- customer identity

products
- product master data

product_variants
- specifications

orders
- order header

order_items
- order details

inventory
- stock management

payments
- payment records


## Rules

- Schema changes require documentation update.
- Migration files are required.
- Avoid storing business data as uncontrolled JSON.
