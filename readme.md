# Tektonia

*The term **builder** (as opposed to user) is employed here to refer to people operating Tektonia.*

Tektonia is an environment for prototyping interactive graphical software. Builders can interact with Tektonia by typing, talking, importing files, drawing or by combining interaction modes. Tektonia produces interfaces with text, 2D and 3D graphics, sounds and images that builders can publish as apps or use as a kit of parts to continue prototyping.

## Hypothesis

Tektonia is also an experiment to prove out a hypothesis: that prioritizing visual representation over text will yield better solutions faster. This advantage should be especially pronounced in fields that are more visually and physically engaged. In other words, building things in the real world rather than the virtual world of bits.

## Principles

Tektonia is intended to be as useful and possible while imposing as few constraints as necessary. A few principles help align decisions with this goal.

  - **Maximize expressiveness.** Builders should feel a driectness between their actions and Tektonia's response. Builder's should be able to use their preferred mode of expression (drawing, writing, movement, etc.) to interact.
  - **Grow to meet needs.** Tektonia should always respond to builders in a helpful manner. If a capability that could help the builder acheive their goals is missing Taktonia should work with builders to grow that new capability.
  - **Respect privacy.** Builders should have the expectation that what they create in Tektonia is their own. Data should only be shared explicitly by builders.
  - **Do not interrupt.** When extending capabilities or changing existing functionality, Tektonia should maintain a seemless experience for the builder. Restarts or other delays should be very rare occurences.

## AI Strategy

Tektonia deeply integrates AI/ML. LLM inference is mediated by an agent framework. Inference "speaks" the types and functions in the core library, combining them into new capabilities. Inference also generates new types and functions to support the new capcbilities. Recompilation and other code processing steps should happen in the background while preserving the live environment that the builder is using.

## Operating system support

Tektonia runs a native app on Linux, macOS, Windows, iOS and Android. It can also be run as a web app.

## Components and dependencies

 - Native application framework: Tauri
 - AI framework: Mastra (TypeScript) or Rig (Rust)
 - Core logic: Rust library using libraries from the Bevy project
 - Server framework: SvelteKit
 - UI component library: Svelte with Typescript bindings to core logic types
