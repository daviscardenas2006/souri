# SOURI Architecture

SOURI is being built as a privacy-first browser extension designed to protect sensitive information before it is sent to AI tools.

This public architecture note describes the product at a high level without exposing sensitive internal implementation details.

## Product model

SOURI operates close to the user input layer.

Its purpose is to help users detect, review, sanitize, and audit sensitive information in prompts before submission. Instead of relying on invisible background behavior, the product is designed to provide visible controls and practical feedback during real workflows.

## Core public components

### 1. Active input detection

SOURI monitors supported input surfaces and evaluates prompt content for sensitive patterns and relevant data categories.

This detection layer is meant to work in real time while the user is interacting with an AI tool.

### 2. In-context action surface

When relevant content is detected, SOURI exposes visible actions through an in-context toast.

This surface is intended to make privacy actions immediate and understandable rather than hidden or abstract.

### 3. Sanitization flow

When the user chooses to sanitize content, SOURI applies a transformation directly to the active input.

The goal is to reduce exposure before the prompt is submitted.

### 4. Local audit trail

SOURI keeps a visible record of relevant privacy events through an audit viewer.

This gives the user a way to review what was detected, what action was taken, and how the product behaved over time.

### 5. Rule creation from real events

A key workflow in SOURI is the ability to turn real audit events into reusable rules.

This allows the product to move from one-off actions toward more durable privacy control.

## Design principles

SOURI is being developed around a few core product principles:

- local-first behavior
- visible user control
- practical, low-friction workflows
- reusable privacy actions
- clear product boundaries

## Public/private boundary

This repository documents the public-facing structure and direction of SOURI.

At this stage, the core implementation remains private while the public materials focus on product architecture, interface direction, workflow design, and privacy principles.
