# ProjrctArbeit_TRFC_Estimation

The friction coefficient between a vehicle's tires and the road surface is a crucial parameter influencing vehicle dynamics. Here, I discuss some of findings.

# Motivation

Have you ever wondered what happens to the tire contact patch when you rotate the steering wheel left and right while the vehicle remains stationary? 
How does this motion influence the shear stress distribution in the contact area? 
And how can this phenomenon be used to estimate the friction coefficient?

## Tire Contact Patch Normal Force Distribution

The distribution of normal force within the tire's contact patch, q_z(x, y) is a critical factor in tire modeling. Various pressure distribution models have been proposed to approximate real tire behavior.

In this work, the normal load distribution is derived by specifying individual distributions in the longitudinal q_zx(x) and lateral q_zy(y) directions, which are then multiplied together:

$$
q_z(x, y) = q_{zx}(x) \cdot q_{zy}(y)
$$

### 1. Quartic load Distribution in Longitudinal and Tapered-off load Distribution in the lateral direction

The longitudinal quartic load distribution \( q_{zx}(x) \) is given by:

$$
q_{zx}(x) = c_4 x^4 + c_3 x^3 + c_2 x^2 + c_1 x + c_0
$$

The value of the constant can be obtain by applying following constraints.
  1. Two Boundary value constraints
  2. Total load
  3. Slope of the normal force
  4. Central load constraint


  ![x_quartic_y_trapezoidal](https://github.com/user-attachments/assets/2d71f62e-70cc-4cb8-a2e8-335972c58ae4)
  *Figure1: Quartic longitudinal load distribution with Tapered-off lateral load distribution.*



### 2. Quartic load Distribution in Longitudinal and Uniform load Distribution in the lateral direction

Uniform Lateral load Distribution:

 $$
 q_{zy}(y) = 1 / 2w
 $$

 Where,

 w = Half width of the patch

 ![x_quartic_y_uniform](https://github.com/user-attachments/assets/423e9986-8876-4d8e-9576-9df6fb3a819f)
 *Figure2: Quartic longitudinal load distribution with Uniform lateral load distribution.*

### 2. Parabolic load Distribution in Longitudinal and Tapered-off load Distribution in the lateral direction

Tapered-off  Lateral load Distribution:

$$
q_z(x,y) = \frac{3F_z}{4a} \left(1 - \left(\frac{x}{a}\right)^2 \right)
$$

Where,

  Fz = Total vehicle load
  
  a = Half-length of the contact patch

  x = Total length of the conatct patch

  ![x_parabolix_y_taperedoff_load_distri](https://github.com/user-attachments/assets/f004193b-1bcc-435a-8822-2d2e4d5dd223)
  *Figure3: Parabolic longitudinal load distribution with tapered-off  lateral load distribution.*

  ## References:

  1. Hans B. Pacejka,Tire and Vehicle Dynamics (Third Edition)

  2. Beal, Craig E., and Sean Brennan. "Friction detection from stationary steering manoeuvres." Vehicle System Dynamics 58.11 (2020): 1736-1765.
