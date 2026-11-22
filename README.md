<p align="center">
  <a href="https://roansystem.com"><img src="assets/banner.png" alt="Roan System: human and machine, one system. Technology studio in Ticino, Switzerland." width="100%"></a>
</p>

**Roan System** is a technology studio in Ticino, Switzerland. One person decides; a crew of AI agents does the work, each with its own craft and limits, and nobody reviews their own output. We build Roan OS, custom agent systems and small robots, and we contribute to open source with real Windows hardware and negative controls.

## Recent contributions

**[R0Y00/Xbox2Windows](https://github.com/R0Y00/Xbox2Windows)**: six pull requests merged by the maintainer.

| PR | Change |
|---|---|
| [#564](https://github.com/R0Y00/Xbox2Windows/pull/564) | Batch the integer and SDWA predicate draws in `pixel_aot`: 168 → 83 draws, the slowest hardware test from ~60 s to ~31 s on an RTX 3070 |
| [#549](https://github.com/R0Y00/Xbox2Windows/pull/549) | Record the `pixel_aot` binary16 denormal mode and draw an f16 subnormal control |
| [#501](https://github.com/R0Y00/Xbox2Windows/pull/501) | Add four verified GPU runs to the README hardware table |
| [#435](https://github.com/R0Y00/Xbox2Windows/pull/435) | Check that the built array-atomics probe keeps `nonUniformIndex`, [requested by the maintainer](https://github.com/R0Y00/Xbox2Windows/issues/369#issuecomment-7072920615) after our DXIL analysis |
| [#445](https://github.com/R0Y00/Xbox2Windows/pull/445) | Check 4 KiB BC7 surface linearization against a bit-order oracle |
| [#348](https://github.com/R0Y00/Xbox2Windows/pull/348) | Run the BC7 block reference check on Linux CI |

**Hardware verification** on Windows 11 + RTX 3070 and WARP:

- [#281](https://github.com/R0Y00/Xbox2Windows/issues/281#issuecomment-7070761909): 2,200 launches with no hang, plus a discrimination test that [another contributor ran](https://github.com/R0Y00/Xbox2Windows/issues/281#issuecomment-7072142809) to pin the cause. The fix, [#394](https://github.com/R0Y00/Xbox2Windows/pull/394), is merged.
- [#312](https://github.com/R0Y00/Xbox2Windows/issues/312#issuecomment-7078022429): our f16 denormal probe, re-run by the issue author on AMD and RTX 3080 with identical results.
- [#521](https://github.com/R0Y00/Xbox2Windows/pull/521#issuecomment-7076896288), [#541](https://github.com/R0Y00/Xbox2Windows/pull/541#issuecomment-7079761460), [#560](https://github.com/R0Y00/Xbox2Windows/pull/560#issuecomment-7079761718): physical-GPU runs for PRs whose CI covers WARP only, each with negative-control mutations that turn red.
- [Our RTX 3070 run](https://github.com/R0Y00/Xbox2Windows/issues/1#issuecomment-7070552394) is listed in the project's [hardware coverage table](https://github.com/R0Y00/Xbox2Windows#hardware-coverage).

## For maintainers

Need a check on real hardware? **Tag @roansystemlabs** for a Windows 11 + RTX 3070 run (D3D12 debug layer, WARP for comparison). Every report states the exact commit, repeats the run, and includes at least one negative control that must fail.

## Links

[roansystem.com](https://roansystem.com/en/) · [Lab notes](https://roansystem.com/en/lab/) · [How we work](https://roansystem.com/en/studio/how-we-work/) · [The team](https://roansystem.com/en/studio/team/)

<sub>AI-assisted studio: founded and directed by Kevin, built with a crew of custom AI agents. Every public contribution is reviewed before it goes out.</sub>
