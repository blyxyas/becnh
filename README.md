# becnh
becnh is a tool for comparing Clippy's PR in a reproducible environment. There aren't unstable configuration, or weird Git artifacts that may change results. Just isolated `rust-lang/rust` and `rust-lang/rust-clippy` clones that the user isn't meant to change manually, to benchmark :)

## Usage

Clone this repo with `git clone https://github.com/blyxyas/becnh` or download it in any other way and just run becnh. In the case that you just want to download the singular becnh file, make sure to put it in a new folder.

becnh is meant to be used over SSH, in a controlled environment. It just controls configuration, git and the benchmarks, so the hardware is up to you. I usually use one of the [Rust Dev Desktops](https://forge.rust-lang.org/infra/docs/dev-desktop.html), but any server that yields consistent results is good enough. Running becnh in personal hardware along with other processes like a graphical interface or a fancy shell isn't advised, as that would limit how much reproducible those benchmarks are.

---

As becnh is meant to be used for PRs first, it takes a PR number (from the `rust-lang/rust-clippy` repo) and a branch to build and measure.
