# SaR_epistemic
Epistemic PDDL of Search and Rescue domain

The Search and Rescue domain and problem files are tested with the  *plank* toolkit to parse, ground, validate plan, and perform *bfs_planner* as a baseline planner to get the plan with Best First Search. These tools are built from the [plank toolkit](https://github.com/a-burigana/plank) for IPC 2026- Epistemic Track. Please refer to the link for details of installation and usage.


## Basic level:
Use domain *sar_domain.epddl* either prob1 or prob2.

Note:
- Problem 1 (sar_prob1.epddl): a simple problem that 3 agents, drone (D1), firefighter (F1), and ambulance (A1) know no fire in anywhere. They need to find victim (move and sense), announce to proper rescue agent (ambulance A1), and rescue the victim.

- Problem 2 (sar_prob2.epddl): 3 agents, drone (D1), firefighter (F1), and ambulance (A1) only know no fire at their current starting location (l0). They need to find victim, investigate if fire is at victim location, extinguish fire if needed, and rescue the victim.

## Intermediate level:
Use domain *sar_domain_intermediate.epddl* with more types of actions. It works with problem 1, 2, and 3.

- Problem 3 (sar_prob3_doxastic.epddl): 3 agents as previous problems, in which drone D1 has no belief and knowledge in victim and fire locations. Firefighter F1 and ambulance A1 has false belief that l2 is safe but in fact there is fire at l2.

## Hard level:
Use domain *sar_domain_hard.epddl* with include non-deterministic action for extinguishing fire. It compiles with problem 1, 2, and 3.
