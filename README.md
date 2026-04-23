# SaR_epistemic
Epistemic PDDL of Search and Rescue domain

The repo also include *plank* to parse, ground, and validate plan, and *bfs_planner* as a baseline planner to get the plan with Best First Search. These tools are built from the [plank toolkit](https://github.com/a-burigana/plank) for IPC 2026- Epistemic Track. Please refer to the link for details of usage.

Here are some simple commands:

## Parse, ground, and export grounding output:

`./plank parse -d <domain path> -p <problem path> [-l [<libraries paths>]...]`

if storing domain, problem, and libraries files in a specification json file

`./plank parse -s <specification path>`

similarly for grounding, by replacing "parse" with "ground"

To export the grounding outputs to a folder 

`./plank -d <domain path> -p <problem path> [-l [<libraries paths>]...] -o <path to directory>`

or 

`./plank export -s <specification path> -o <path to directory>`

For more details of *plank*, run: `./plank --help`

## Plan with BFS
`./bfs_planner -d <domain path> -p <problem path> [-l [<libraries paths>]...] [--plan-file <plan file path>]`

or

`./bfs_planner -s <specification path> [--plan-file <plan file path>]`

More details, run: `./bfs_planner --help`