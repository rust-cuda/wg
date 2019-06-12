# CUDA WG - draft

## What value do you want to bring to the project?

The Working Group's goal is to deliver first-class CUDA support to Rust users - see our [Roadmap].

[Roadmap]: https://github.com/rust-cuda/wg/blob/master/documents/roadmap.md

## Why should it be put into place?

The WG is already in place as an unofficial WG, see our [Github], [Roadmap], [Zulip], and some PRs by WG members: [rust@denzp], [rust@peterhj], [stdsimd], [libc], etc.

Being an official WG would allow us to use the official communication channels like the rust-lang zulip, which would give us more visibility and allow us to attract more contributors.

[Github]: https://github.com/rust-cuda
[Zulip]: https://rust-cuda.zulipchat.com/
[libc]: https://github.com/rust-lang/libc/pull/1126
[stdsimd]: https://github.com/rust-lang-nursery/stdsimd/pulls?q=is%3Apr+nvptx+is%3Aclosed
[rust@denzp]: https://github.com/rust-lang/rust/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Aclosed+author%3Adenzp
[rust@peterhj]: https://github.com/rust-lang/rust/pulls?utf8=%E2%9C%93&q=is%3Apr+is%3Aclosed+author%3Apeterhj

## What is the working group about?

Right now, this WG is about making the already-existing Rust CUDA support minimally reliable.
Getting a safe and production-ready development experience on Stable Rust is our primary goal!

Also, currently a major obstacle for developing GPGPU applications and algorithms in Rust is a lack of learning resources.
We plan to solve the "documentation debt" with a broad range of tutorials, examples and references.

## What is the working group not about?

The WG is not focused on promoting or developing "standard" frameworks.
Instead, we want to provide basic and reliable support of the feature and inspire the community to start using it.

This WG is only about CUDA support - other GPGPU targets are out-of-scope.
Our focus is on making the current CUDA target more reliable.
Everything that goes beyond that (e.g. higher-level CUDA libraries, CUDA frameworks, etc.) is also out-of-scope.

## Is your WG long-running or temporary?

The CUDA WG is long-running. We have a [Roadmap] for an MVP, but there are many issues worth solving once that MVP is achieved (e.g. foundational libraries).

In the end, we hope the WG will evolve into another one to cover similar topics:
to support other GPGPU platforms or to create higher-level frameworks to improve end-to-end experience based on community feedback.

## What is your long-term vision?

Having a reliable and safe CUDA development experience is our ultimate goal.
To get there, first of all, we will need to achieve all milestones in our [Roadmap].

## How do you expect the relationship to the project be?

The Working Group is mainly going to create various RFCs and send PRs to Rust components.

An important aspect of the WG is active participation in discussions related to the NVPTX target and involved tools.
This also includes [already reported issues](https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AO-NVPTX) and those that will be opened due to the work made by the WG.

### How do you want to establish accountability?

Currently, as an unofficial WG, we work completely in the open and we intend to go on in the same way.
Most of discussions happen either in out github issues, or in our public [Zulip], so that they be read by anyone.

Once we will start having regular meetings, we would publish agenda and summary.

## Which other WGs do you expect to have close contact with?

We would like to cooperate with *Language Team* (or perhaps, additionally with *Unsafe Code Guidelines WG*) in discussions about safety in SIMT code.
Additionally, it would be very important to discuss with *Infra team* a strategy of reliable deployment of `rust-ptx-linker` (likely as a `rustup` component).

On the other hand, proposed [Machine Learning WG](https://internals.rust-lang.org/t/enabling-the-formation-of-new-working-groups/10218/11) could leverage CUDA accelerated computing capabilities, so we can collaborate on their use cases.

## What are your short-term goals?

Mainly, short-term goals are defined in our [Roadmap] for an MVP.
Additionally, we plan to make a poll about use cases, expectations, and community awareness that it is already possible to experiment with CUDA on Nightly Rust today.

## Who is the initial leadership?

> TBD...

## How do you intend to make your work accessible to outsiders?

Blog posts, announcements and retrospective about made decisions should help to get more people involved in either discussions or further experimenting.

## Everything that is already decided upon

We work in the open, see our [Github].

## Preferred way of contact/discussion

[Github] issues or [Zulip].
