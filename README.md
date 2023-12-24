# AISE: A Symbolic Verifier by Synergizing Abstract Interpretation and Symbolic Execution	

AISE is a static verifier that combines abstract interpretation and symbolic execution techniques. The verification approach is based on a verification framework that combines abstract interpretation and symbolic execution in a novel way. 

## Implementation
AISE is implemented based on Clam ([https://github.com/seahorn/clam](https://github.com/seahorn/clam)) and KLEE ([https://github.com/klee/klee](https://github.com/klee/klee)).
AISE also calls ESBMC (https://github.com/esbmc/esbmc) when it detects programs containing floating-point data (less than 50 programs have floating-point data in the ReachSafety-Loops category), because AISE is unable to handle floating-point data. (AISE doesn't link against ESBMC, it only calls it in special cases.).

## Usage

## verify C program
/bin/aise <input C file>
e.g. ./bin/aise ./bin/array-1.c
## version
./bin/aise --version 

## about SV-COMP2024
It's the first time we try to particapate in SV-COMP, we only focus on a single category "Reachability-Loops". AISE ranked 5th in this category, the results can be found here: (https://sv-comp.sosy-lab.org/2024/results/results-verified/). AISE's archive is publicly avaliable in https://doi.org/10.5281/zenodo.10201159. 
