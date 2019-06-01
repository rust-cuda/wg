# CUDA WG - draft

## What value do you want to bring to the project?

The Working Group is an attempt to combine efforts to bring reliable support of writing safe GPGPU CUDA code with Rust.
The work that will be done is supposed to clear the path for other GPGPU platforms in future.

## Why should it be put into place?

First steps to basic support of the feature have already been made by individual developers.
Regardless of recent progress, there are still a lot of questions about safety and soundness of SIMT (Single Instruction, Multiple Threads) code and they require a lot of collaboration to find solutions.

## What is the working group about?

We want to work together on getting a solid foundation for writing CUDA code.
Getting a safe and production-ready development experience on Stable Rust is our primary goal!

Also, currently a major obstacle for developing GPGPU applications and algorithms in Rust is a lack of learning resources.
We plan to solve the "documentation debt" with a broad range of tutorials, examples and references.

## What is the working group not about?

The WG is not focused on promoting or developing "standard" frameworks.
Instead, we want to provide basic and reliable support of the feature and inspire the community to start using it.
This should lead to experimenting with different approaches on how to use it and creating awesome tooling.

## Is your WG long-running or temporary?

In our current vision, the WG should live until we fulfill our goals.

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

We would like to cooperate with Core or Compiler Teams in discussions about safety in SIMT code.
Additionally, it would be very important to discuss a strategy of reliable deployment of `rust-ptx-linker` (likely as a `rustup` component).

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

We already have a [`rust-cuda`](https://github.com/rust-cuda) Github organization and a [`rust-cuda`](https://rust-cuda.zulipchat.com) Zulip server.

> TBD... would it make sense to move to a `rust-lang` Zulip server?

## Where do you need help?

> TBD...

## Preferred way of contact/discussion

> TBD...
