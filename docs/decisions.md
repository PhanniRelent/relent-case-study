# Product and Technical Decisions

## Keep the primary experience usable without an account

Account creation adds friction at the moment a user is trying to understand the product. The core flow therefore starts locally, while cloud continuity is optional.

**Tradeoff:** local-first behavior requires explicit handling for later sign-in, account switching, synchronization, and conflict resolution.

## Use deterministic logic for the core result

Structured, inspectable rules make important product behavior easier to test and review than an unconstrained model response.

**Tradeoff:** deterministic systems require careful authoring, versioning, and maintenance as the product vocabulary grows.

## Treat AI as a bounded capability

AI can help with flexible language and iteration, but the product should have a clear fallback when an external model is unavailable or inappropriate.

**Tradeoff:** maintaining both bounded AI behavior and deterministic fallback paths creates additional testing and compatibility work.

## Separate local and cloud trust boundaries

Local values and synchronized content have different operational risks. They are handled as separate persistence and key-management concerns.

**Tradeoff:** encryption reduces exposure but does not justify claiming that a server-accessible design is zero-knowledge.

## Make safety affect available behavior

Safety-sensitive states should change which paths can be shown or taken. They should not be treated as ordinary personalization signals.

**Tradeoff:** conservative gating can reduce flexibility, so it requires deliberate product and content review.
