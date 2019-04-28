# swim
Swim With Individualized Modules

The SWIM pseudocode intends to provide workouts for individuals with an intensity scale from 0 to 10 based on swimming capabilities and time available.
Each set is expected to be completed in a 2 hour session and should help develop specific strokes or skills for swimmers.

Each set assumes the following:

- `IM = {Butterfly, Backstroke, Breaststroke, Freestyle}`: Individual Medly (IM) is an array containing the 4 competition strokes in the defined order. Arrays in SWIM allow for negative indexing, such that `IM[-1] = Freestyle`. Indexing starts at 0 such that `IM[0] = Butterfly`
- `set s(scale, pool_type){}`: this is equivalent to the `def f(x)` notation in languages like python, but notably contains braces to help swimmers easily find the start and end of each set block
	- `scale` is a scale from 0 to 10, where 0 skips all sets except for warm-up and cool-down, and 10 is for professional swimmers (approximated)
	- `pool_type` is one of the following:
		- `scy`: short-course yards
		- `scm`: short-course meters
		- `lcm`: short-course meters
- `swim(stroke, distance, intensity)` and swim(stroke, distance, intensity, style)` are the primary building blocks for swimming sets and will be provided without further elaboration.
	- `stroke` may be any stroke, including: `butterfly`, `backstroke`, `breastroke`, `freestyle`, `scull`, `doggy`
	- `distance` is provided in either meters or yards, depending on the pool available. For most applications of SWIM, short-course meters are assumed; however
	- `intensity` is defined with the following keywords:
		- `easy`: no more than 25% intensity
		- `medium`: 50% intensity
		- `strong`: 75% intensity
		- `hard`: 90% intensity
		- `sprint`: 100% intensity
	- `style` is an optional argument that allows for variations on each stroke, such as `kick`, and `drill`, or specific drills like `zipper` for `freestyle`.
- `for (i = n:m){}` will iterate through all elements between `n` and `m`, starting at `n` and ending at `m-1`
- `from setfile import s` will allow for importing sets from one SWIM file to another
- comments are made with the `#` character

All sets will be in the `sets` directory with the `.swim` extension.

The SWIM pseudocode was largely inspired as a mix between julia, python, and C syntaxes and is intended to be used for personal use; however, please feel free to modify this notation at will and even submit a PR with your favorite work-out of choice!

As a huge disclaimer, I am not a swim coach, I just wanted to write my workouts in pseudocode.
