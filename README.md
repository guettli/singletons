# Singletons

## From Polytheism to Monotheism

While reading Yuval Noah Harari’s *Sapiens*, I struck upon a analogy regarding the evolution of
religion. Harari describes how human history shifted from **Polytheism**—a crowded pantheon of local
gods for specific needs—to **Monotheism**, the belief in a single, all-encompassing "One God" that
governs everything.

As I looked at the modern software landscape, I realized the exact same thing is happening to our
tools.

In the early days of any tech category, we have a "Pantheon." There are dozens of competing
frameworks and implementations, each with its own tribe of followers. But over time, the "market
share ratio" begins to warp. One tool becomes so dominant, so reliable, and so integrated into the
fabric of our work that its rivals effectively disappear.

In software engineering, we have a name for a unique instance that stands alone: a **Singleton**.

## The Rise of the Singleton

When an open-source tool reaches a certain "Threshold of Dominance", it stops being just a choice.
It becomes a **Singleton Implementation**.

This article maintains a list of these "Open Source Monopolies"—the tools that do one thing so well
that the second alternative has been almost rendered obsolete.

## Defining the Singleton

To distinguish a Singleton from a merely popular tool or a standard, we use a specific "Threshold of
Dominance":

> **The 10x Dominance Rule:** A Singleton is defined by an adoption rate at least **10 times
    greater** than its closest competitor, effectively rendering the runner-up a niche alternative
    rather than a viable general-purpose rival.

When the gap between the first and second place is this vast, the "Pantheon" of choice has
effectively collapsed into a single implementation.

**Implementation, Not Specification:** A Singleton must be a concrete tool or codebase. Abstract
standards (like **TCP/IP**, **HTTP**, or **SQL**) are not Singletons; they are the protocols that
allow competition to exist.

## The Singleton List

Applying the **10x Dominance Rule**, the following tools qualify as Singleton Implementations. The
table is sorted by the **Dominance Ratio** (Singleton Adoption / Competitor Adoption).

| Tool | Context | Est. Adoption | Closest Competitor | Est. Adoption | Ratio |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **SQLite** | Embedded Database | ~98% | BerkeleyDB | <1% | **~98x** |
| **Kubernetes** | Orchestration | ~62% | HashiCorp Nomad | ~2% | **~31x** |
| **Python** | Machine Learning | ~87% | R | ~4% | **~21.7x** |
| **Git** | Version Control | ~93% | Subversion (SVN) | ~5% | **~18x** |
| **Bash** | Shell Scripting | ~85% | Zsh | ~5% | **~17x** |
| **Flutter** | Cross-platform Self-Rendering UI | ~42% | Qt (Mobile/Desktop) | ~3% | **~14x** |
| **Golang** | Kube Operator Dev | ~71% | Python | ~7% | **~10.1x** |
| **Linux** | Public Cloud OS | ~90% | Windows Server | ~10% | **~9x** |
| **Docker** | Development Tooling | ~77% | Podman | ~14%* | **~5.5x** |

*\*Note: As seen with Docker vs. Podman, some former Singletons are losing their 10x status as the
"Pantheon" begins to re-emerge. Estimates based on Stack Overflow 2023/2024 surveys and CNCF
landscape reports.*

### Notes on Classification

**Flutter vs. React Native:** React Native is excluded from the "Self-Rendering" comparison because it relies on native host-platform widgets (the "Bridge" approach). Flutter is a Singleton specifically within the category of frameworks that provide their own self-contained rendering engine (Skia/Impeller).

**C and C++:** These are excluded from the list because they are languages (specifications) rather than specific implementations. Their compiler ecosystem remains a classic "Pantheon" (GCC, Clang, MSVC) where no single implementation reaches the 10x dominance threshold.

## Drawbacks

While Singletons provide industry-wide standardisation, they come with significant risks:

* **Innovation Stagnation:** Without the pressure of a close competitor, the incentive to simplify
    or improve the tool diminishes.
* **Single Point of Failure:** A critical security vulnerability or architectural flaw in a
    Singleton becomes a systemic risk for the entire software industry.
* **High Barrier to Entry:** New paradigms are often discarded simply because they lack the massive
    ecosystem and integration support of the reigning Singleton.

## More

* [Deadends of IT](https://github.com/guettli/deadends-of-it)
* [Thomas WOL: Working out Loud](https://github.com/guettli/wol)
