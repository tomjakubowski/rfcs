- Start Date: (fill me in with today's date, YYYY-MM-DD)
- RFC PR: (leave this empty)
- Rust Issue: (leave this empty)

# Summary

Extend the notion of sequence repetition on `TtSequence` trees to include
optional sequences of trees with a regex-like syntax: `$(...)?`.  This
simplifies `macro_rules` macros with optional sections by not requiring
redundant matchers

# Motivation

Why are we doing this? What use cases does it support? What is the expected outcome?

# Detailed design

This is the bulk of the RFC. Explain the design in enough detail for somebody familiar
with the language to understand, and for somebody familiar with the compiler to implement.
This should get into specifics and corner-cases, and include examples of how the feature is used.

notes:

# Drawbacks

Why should we *not* do this?

* Doesn't cover a common use case like `$(pub)?` b/c no captures

# Alternatives

* zz
* generalize this with `$(...){m,n}` for a sequence repeated `[m,n]` times.
FIXME

# Unresolved questions

What parts of the design are still TBD?
* should they allow separators? doesn't really make sense
* backwards compatible? consider `?` used as a separator today: `$(...)?*`.

