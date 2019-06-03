# CUDA WG - draft

## What value do you want to bring to the project?

The Working Group's goal is to deliver first-class CUDA support to Rust users - see our [Roadmap].

[Roadmap]: https://github.com/rust-cuda/wg/blob/master/documents/roadmap.md

The work that will be done is supposed to clear the path for other GPGPU platforms in future.

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
This WG is only about CUDA support - other GPGPU targets are out-of-scope. Our focus is on making the current CUDA target more reliable. Everything that goes beyond that (e.g. higher-level CUDA libraries, CUDA frameworks, etc.) is also out-of-scope.

## Is your WG long-running or temporary?

The CUDA WG is long-running. We have a [Roadmap] for an MVP, but there are many issues worth solving once that MVP is achieved (e.g. foundational libraries).

In the end, we hope the WG will evolve into another one to cover similar topics:
to support other GPGPU platforms or to create higher-level frameworks to improve end-to-end experience based on community feedback.

## What is your long-term vision?

Having a reliable and safe CUDA development experience is our ultimate goal.
This should include:

* Getting `nvptx64-nvidia-cuda` to a [Tier 2](https://forge.rust-lang.org/platform-support.html) support state.
* Test infrastructure on a real hardware and running the tests during Rust CI process.
* Rich documentation, references, tutorials and examples.
* A broad set of new compile errors, warnings and lints for SIMT execution model to avoid pitfalls and ensure code soundness.

## How do you expect the relationship to the project be?

The WG will be responsible for CUDA related issues and user requests.
This includes [already reported issues](https://github.com/rust-lang/rust/issues?q=is%3Aopen+is%3Aissue+label%3AO-NVPTX) and those that will be opened due to the work made by the WG.
An important aspect is that the WG will take care of the state of the `rust-ptx-linker` and will do its best to avoid blocking someone else's work (like it, unfortunately, happened in [rust#59752](https://github.com/rust-lang/rust/pull/59752)).

### How do you want to establish accountability?

For that purpose, we will publish an agenda and made decisions from our meetings.
Once we achieve important milestones we plan to make public announces.

## Which other WGs do you expect to have close contact with?

We would like to cooperate with *Language Team* in discussions about safety in SIMT code.
Additionally, it would be very important to discuss with *Infra team* a strategy of reliable deployment of `rust-ptx-linker` (likely as a `rustup` component).

On the other hand, proposed [Machine Learning WG](https://internals.rust-lang.org/t/enabling-the-formation-of-new-working-groups/10218/11) could leverage CUDA accelerated computing capabilities, so we can discuss their use cases.

## What are your short-term goals?

Mainly, short-term goals are about evaluating and discussing how can we achieve long-term goals:

* Make a poll about community experiences and use cases for CUDA.
* Deploy the `rust-ptx-linker` as a `rustup` component.
* Collect soundness and safety issues that can happen in SIMT execution model.
* Decide testing approach on a real hardware.

## Who is the initial leadership?

> TBD...

## How do you intend to make your work accessible to outsiders?

Excessive learning materials and retrospective about made decisions should help to get more people involved in either discussions or further experimenting.

> TBD... something else?

## Everything that is already decided upon

We work in the open, see our [Github].

> TBD... would it make sense to move to a `rust-lang` Zulip server?

## Preferred way of contact/discussion

[Github] issues or [Zulip].
