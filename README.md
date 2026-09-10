# Trading Bot — project overview

This document describes a private, single-user application in the design stage. It is published for review of the proposed Reddit Data API integration. This repository is documentation only; it does not contain a working bot or claim approved Reddit access.

## Purpose

The planned application combines public investing discussion, news and market data to support automated trading in its owner's brokerage account. It is for personal use, not a public subscription service or academic research project. Reddit discussion is treated as unverified evidence, not as an instruction to trade.

## Proposed Reddit integration

- Read public posts and selected comments from r/wallstreetbets, r/investing, r/stocks, r/options, r/SecurityAnalysis and r/ValueInvesting.
- Use approved OAuth access with the read scope. No posting, voting, messaging, moderation or access to private communities is requested.
- Identify ticker discussions and linked news, compare claims with independent sources, and assess sentiment and potential risks.
- Process relevant excerpts through external AI inference providers: OpenAI, Anthropic, xAI, DeepSeek and Google. No model training on Reddit content is planned. Such processing is contingent on Reddit's permission and applicable provider terms.
- Apply a shared ceiling of 30 requests per minute, reduced if the approved allowance is lower. Respect rate-limit responses and backoff.
- Retain raw content for at most 48 hours, check for deletions hourly, and propagate discovered deletions to retained excerpts and content-bearing derived records, indexes and backups.

These are proposed controls, not implemented capabilities. Reddit ingestion will remain disabled until approval and implementation are complete. Any approval conditions take precedence over the proposed collection, processing and retention design.

## Deployment and status

The application is intended to run on an owner-controlled computer, with external API connectors and a separate deterministic execution component. It is not an interactive app installed inside a subreddit. API credentials, brokerage details and private application files are excluded from this overview.

Reddit access, pricing, permitted external AI processing and retention remain subject to review. This page is not a source-code release or an assertion that the project meets all access requirements. Source code or additional documentation can be provided through an agreed review process if required.
