# WuMama-System Repository Plan

Version: v0.7

## Purpose

Define the next development repository after Enterprise OS documentation is stable.

Repository:

WuMama-System

Purpose:
Actual software development.


## Repository Structure

WuMama-System

frontend/
- Next.js customer website

backend/
- Node.js API services

supabase/
- Database migrations
- SQL
- RLS policies

admin/
- Internal operation dashboard

tests/
- Automated testing

docs/
- Technical documents


## Development Start

Phase 0:

Project initialization

Tasks:
- Create Next.js project
- Configure Tailwind
- Connect Supabase
- Setup environment variables
- Setup Git workflow


## Migration Strategy

Current:

HTML/CSS/JS + Supabase

Target:

Next.js + API + Supabase


Migration principle:

Do not rewrite everything at once.

Move feature by feature.
