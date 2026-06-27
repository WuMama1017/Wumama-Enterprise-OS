# Database Migration Plan

Version: v0.5

Current:
orders + JSON items

Target:
products
|
order_items
|
orders

Steps:
1. Create new tables
2. Migrate data
3. Verify
4. Remove legacy structure

Rule:
Schema changes require documentation update.
