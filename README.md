<p align="center">
  <a href="https://roansystem.com"><img src="assets/banner.png" alt="Roan System: human and machine, one system. Technology studio in Ticino, Switzerland." width="100%"></a>
</p>

**Roan System** is a technology studio in Ticino, Switzerland. One person decides; a crew of AI agents does the work, each with its own craft and limits, and nobody reviews their own output. We build Roan OS, custom agent systems and small robots, and we contribute to open source with real Windows hardware and negative controls.

## Recent contributions

**[R0Y00/Xbox2Windows](https://github.com/R0Y00/Xbox2Windows)**: 15 pull requests merged by the maintainer as of 23 November 2026 ([full list](https://github.com/R0Y00/Xbox2Windows/pulls?q=is%3Apr+author%3Aroansystemlabs+is%3Amerged)).

| PR | Change |
|---|---|
| [#776](https://github.com/R0Y00/Xbox2Windows/pull/776) | Lower a per-lane compute guard as control flow around its stores (step 2 of [#721](https://github.com/R0Y00/Xbox2Windows/issues/721)) |
| [#773](https://github.com/R0Y00/Xbox2Windows/pull/773) | Cast a shadow with a translated depth pass and `SampleCmpLevelZero` (shadow step of [#730](https://github.com/R0Y00/Xbox2Windows/issues/730)) |
| [#750](https://github.com/R0Y00/Xbox2Windows/pull/750) | Accept the LLVM 15 group-base form of a compute byte offset (follow-up to [#724](https://github.com/R0Y00/Xbox2Windows/pull/724)) |
| [#749](https://github.com/R0Y00/Xbox2Windows/pull/749) | Light a translated mesh draw with an interpolated normal and N·L (lighting step of [#730](https://github.com/R0Y00/Xbox2Windows/issues/730)) |
| [#738](https://github.com/R0Y00/Xbox2Windows/pull/738) | Extract two-exit compute programs with the #477 check (step 1 of [#721](https://github.com/R0Y00/Xbox2Windows/issues/721)) |
| [#718](https://github.com/R0Y00/Xbox2Windows/pull/718) | Lower `image_sample_c_lz` to `SampleCmpLevelZero` in `pixel_aot`: shadow-map sampling in translated pixel shaders |
| [#708](https://github.com/R0Y00/Xbox2Windows/pull/708) | Accept 2D/3D and wider thread groups in `compute_store_aot`, from our issue [#701](https://github.com/R0Y00/Xbox2Windows/issues/701) |
| [#699](https://github.com/R0Y00/Xbox2Windows/pull/699) | `disasm_rdna2`: decode `s_waitcnt` with the GFX10 counter fields |
| [#693](https://github.com/R0Y00/Xbox2Windows/pull/693) | `disasm_rdna2`: consume the second dword of DPP, SDWA and literal-K forms |
| [#564](https://github.com/R0Y00/Xbox2Windows/pull/564) | Batch the integer and SDWA predicate draws in `pixel_aot`: 168 → 83 draws, the slowest hardware test from ~60 s to ~31 s on an RTX 3070 |
| [#549](https://github.com/R0Y00/Xbox2Windows/pull/549) | Record the `pixel_aot` binary16 denormal mode and draw an f16 subnormal control |
| [#501](https://github.com/R0Y00/Xbox2Windows/pull/501) | Add four verified GPU runs to the README hardware table |
| [#445](https://github.com/R0Y00/Xbox2Windows/pull/445) | Check 4 KiB BC7 surface linearization against a bit-order oracle |
| [#435](https://github.com/R0Y00/Xbox2Windows/pull/435) | Check that the built array-atomics probe keeps `nonUniformIndex`, [requested by the maintainer](https://github.com/R0Y00/Xbox2Windows/issues/369#issuecomment-7072920615) after our DXIL analysis |
| [#348](https://github.com/R0Y00/Xbox2Windows/pull/348) | Run the BC7 block reference check on Linux CI |

**Open:** [#788](https://github.com/R0Y00/Xbox2Windows/pull/788), copy compute buffer reads from a caller-bound source to the store (step 3 of #721).

**Chapters proposed by the studio and approved by the maintainer:**

- [#721](https://github.com/R0Y00/Xbox2Windows/issues/721), two-exit and guarded compute programs: steps 1 and 2 merged (#738, #776), step 3 open (#788).
- [#730](https://github.com/R0Y00/Xbox2Windows/issues/730), a lit, shadowed scene through the translated mesh and pixel stages: lighting (#749) and shadow (#773) merged; wiring the scene to the EXE remains.

**Hardware verification** on Windows 11 + RTX 3070 and WARP:

- [#281](https://github.com/R0Y00/Xbox2Windows/issues/281#issuecomment-7070761909): 2,200 launches with no hang, plus a discrimination test that [another contributor ran](https://github.com/R0Y00/Xbox2Windows/issues/281#issuecomment-7072142809) to pin the cause. The fix, [#394](https://github.com/R0Y00/Xbox2Windows/pull/394), is merged.
- [#312](https://github.com/R0Y00/Xbox2Windows/issues/312#issuecomment-7078022429): our f16 denormal probe, re-run by the issue author on AMD and RTX 3080 with identical results. The probe is now its own project, [gpu-denorm-probe](https://github.com/roansystemlabs/gpu-denorm-probe).
- [#521](https://github.com/R0Y00/Xbox2Windows/pull/521#issuecomment-7076896288), [#541](https://github.com/R0Y00/Xbox2Windows/pull/541#issuecomment-7079761460), [#560](https://github.com/R0Y00/Xbox2Windows/pull/560#issuecomment-7079761718): physical-GPU runs for PRs whose CI covers WARP only, each with negative-control mutations that turn red.
- [Our RTX 3070 run](https://github.com/R0Y00/Xbox2Windows/issues/1#issuecomment-7070552394) is listed in the project's [hardware coverage table](https://github.com/R0Y00/Xbox2Windows#hardware-coverage).

## For maintainers

Need a check on real hardware? **Tag @roansystemlabs** for a Windows 11 + RTX 3070 run (D3D12 debug layer, WARP for comparison). Every report states the exact commit, repeats the run, and includes at least one negative control that must fail.

## Links

[roansystem.com](https://roansystem.com/en/) · [Lab notes](https://roansystem.com/en/lab/) · [How we work](https://roansystem.com/en/studio/how-we-work/) · [The team](https://roansystem.com/en/studio/team/)

<sub>AI-assisted studio: founded and directed by Kevin, built with a crew of custom AI agents. Every public contribution is reviewed before it goes out.</sub>
