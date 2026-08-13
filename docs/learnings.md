# Learnings

## Requirements must remain visible after implementation starts

As the product grew, a plausible screen or result was not enough. I needed explicit product rules, boundaries, and testable acceptance criteria so implementation could be checked against intent.

## AI output needs an evaluation loop

AI development tools are most useful when their output is treated as a draft to inspect. My workflow improved when I separated problem definition, generation, review, testing, and product judgment.

## Privacy is an architectural property

Privacy language cannot compensate for an unclear data flow. Mapping what stays local, what reaches a backend, and what reaches an external service made both implementation and product communication more accurate.

## Compatibility becomes part of product ownership

Once a product stores user state, older formats and installed versions affect what can safely be removed. Migration and deprecation decisions need evidence rather than assumptions.

## Testability influences product design

Deterministic, versioned behavior creates more opportunities for regression tests. Large stateful surfaces and device-level journeys still require a separate testing strategy.
