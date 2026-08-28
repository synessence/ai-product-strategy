# Kill Switch Audit

## Vendor Dependency Assessment

| Dimension | Current State | Risk Level | 48-Hour Action |
|-----------|--------------|------------|---------------|
| **Provider** | L | M | make all calls behind AI_gateway function to be platform agnostic |
| **Abstraction** | H | L | calls a generic interface/ML abstraction |
| **Routing** | H | H | Explore routing to foundation model based on real-time cost |
| **Eval** | H | H | Introduce AI evals system to be applied across as models |

## Portability Score
Partial

## If [primary vendor] doubles pricing tomorrow:
Switch to another model OR use open-weight model

## If [primary vendor] ships a competing product:
Unlikely given restricted and regulated data access.
