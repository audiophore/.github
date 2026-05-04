<p align="center">
  <img src="https://raw.githubusercontent.com/audiophore/.github/main/profile/audiophore-lockup-dark-bg.svg" alt="Audiophore" width="600">
</p>

> A high-performance bridge between [Synesthesia](https://getsynesthesia.com/)
> and the wider lighting ecosystem — Hue, WLED, Nanoleaf, DMX, lasers, and beyond.

---

### The name

*Audiophore* — from *audio* + the Greek *-phore* (φόρος, "bearer" or
"carrier"), as in *semaphore* (sign-bearer) or *phosphor* (light-bearer).
An audiophore carries audio. This one carries audio analysis into the
lighting domain — turning what a kick drum, a bass swell, or a scene
change in Synesthesia *means* into what every light, panel, fixture,
and laser in the room *does*.

### What we're building

A single piece of software that lets a performing VJ or DJ write **one
show file** describing how lighting should react to their music — and
have it adapt to whatever hardware is actually present at the venue.
Sub-30ms kick-drum-to-light latency. Open source. Built in Rust.

The bridge subscribes to Synesthesia's OSC stream — FFT bands, beat
detection, BPM tracking, scene palettes — and translates that into
native protocols for whatever lighting hardware happens to be on the
network. Hue Entertainment for living-room ambient, sACN/E1.31 for
WLED strips and panels, Art-Net for venue DMX rigs, Ether Dream for
ILDA lasers, and OSC passthrough for software like Liberation and
Resolume.

### Why this exists

Synesthesia is exceptionally good at audio analysis and shader-driven
visuals, but its lighting integrations end at "screen output." Resolume
DMX is clunky. TouchDesigner can do anything, but only if you *are*
already a TouchDesigner programmer. Hue, Nanoleaf, and WLED users have
no good path to real-time, beat-locked, scene-aware control from VJ
software. Laser people live in their own walled garden.

There's no universal bridge. Audiophore is that bridge.

### Status

🚧 &nbsp; **Pre-implementation, planning phase.** &nbsp; Hardware ordered. M1 milestone
(Synesthesia → WLED proof-of-life) starts when the dev rig arrives.

Watch this space, or follow [@iammrcupp](https://github.com/iammrcupp).

### Tech

🦀 &nbsp; Rust workspace · &nbsp; 🌙 &nbsp; Lua scripting for show logic · &nbsp; 📡 &nbsp; OSC, sACN,
Art-Net, DDP, DTLS · &nbsp; 🐳 &nbsp; ARM64 container target · &nbsp; ☸️ &nbsp; Kubernetes-deployable

### Roadmap

| | Milestone | Scope |
|---|---|---|
| **M1** | Proof of life | Synesthesia OSC → WLED via E1.31, hardcoded |
| **M2** | Real engine | TOML+Lua show files, Hue + Art-Net adapters, web UI |
| **M3** | Lasers + polish | Ether Dream, Liberation passthrough, portable shows, public release |
| **M4+** | Beyond v1.0 | Hardware appliance, marketplace, plugin SDK |

### Get involved

Not yet — but soon. Once M1 lands the repos go public and contributions
open up. If you're a VJ, DJ, lighting tech, or Rust-curious developer
who's been wanting exactly this thing, drop a star on the repo when it
appears or follow along.

### License

MIT OR Apache-2.0 (planned, dual-licensed in the Rust ecosystem standard).
