# ProjectArbeit_TRFC_Estimation
Estimation of the Tire Road Friction Coefficient during stationary and slow moving positions

The friction coefficient between a vehicle's tires and the road surface is a crucial parameter influencing vehicle dynamics. Here, I discuss some of findings.

# Tire Contact Patch Normal Force Distribution

The distribution of normal force within the tire's contact patch, \( q_z(x, y) \), is a critical factor in tire modeling. Various pressure distribution models have been proposed to approximate real tire behavior, including uniform, parabolic, and quartic distributions. These models are typically defined along a single direction and can be combined to represent lateral and longitudinal components. 

In this work, the normal load distribution is derived by specifying individual distributions in the longitudinal (\( q_{zx}(x) \)) and lateral (\( q_{zy}(y) \)) directions, which are then multiplied to obtain the combined distribution:

\[
q_z(x, y) = q_{zx}(x) \cdot q_{zy}(y)
\]


