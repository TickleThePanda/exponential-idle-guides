---

description: "Distribution Overpushing concept."
author: "Playspout"
contributors: "the Amazing Community"
draft: false
order: 0
---




## Distribution Overpushing

### What is distribution overpushing?

A greedy way to push a theory distribution is to push all 8 original theories until they have similar tau/hour gains. However, this is not necessarily optimal for long term tau gains. Distribution overpushing is when you push certain theories such that their tau/hours are less than others. This seems to contradict optimal play, as generally you'd gain more students quicker if you push all theories to equal rates. However, some theories do not benefit as much from the 3rd level of the 9th Research in the Students tab (3R9). Therefore it makes more sense to push theories that don't benefit much from additional students first. This allows us to use the additional students to accelerate the rates of theories that do benefit significantly from 3R9. 

### How theories are affected by additional students

We will compare the effect of students on taudot, vs the effect of time on taudot for each theory. For the equations below, 'K' and 'A' are just constants, 'S' is the multiplier gained from having students (3R9 multiplier).

#### Theory 1

We know that in theory 1, the c4 term dominates late game: <br>
\\(\dot{\rho} = KS\rho^{0.3}\\) <br>
\\(\rho = (KSt)^{0.7}\\) <br>

Despite the 0.7 power, we can conclude that sigma and time affect rho equally. 


#### Theory 2

\\(\dot{q_4}, \dot{r_4} = A; q_4, r_4 ~= At\\)

By the same logic: <br>
\\(\dot{q_3}, \dot{r_3} = At; q_3, r_3 ~= At^2\\) <br>
\\(\dot{q_2}, \dot{r_2} = At^2; q_2, r_2 ~= At^3\\) <br>
\\(\dot{q_1}, \dot{r_1} = At^3; q_1, r_1 ~= At^4\\) <br>
\\(\dot{\rho} ~= (At^{4}At^{4})^{1.15} ~= At^{9.2}\\) <br>
\\(\rho ~= KSt^{10.2}\\) <br>

Here we see that time affects rho 10.2 magnitude higher than extra sigma. 

#### Theory 3

\\(\dot{\rho_n} ~= A, \rho ~= KSt \\) <br>

Sigma and time affect rho equally. 

#### Theory 4

Late game c3 term dominates so: <br>

\\(\dot{\rho} ~= Ac_3q \\) <br>
\\(\dot{q} ~= \frac{A}{1+q} \\) <br>

Solving the differential equation yields q is proportional to \\(\sqrt{t} \\) <br>

\\(\dot{\rho} ~= Ac_3\sqrt{t}\\) <br>
\\(\rho ~= KSt^{1.5}\\) <br>

Time affects rho 1.5 magnitude more than sigma.

#### Theory 5

Late game we can treat c2 gains as instantaneous, so q is treated as a constant.<br>

\\(\dot{rho} ~= A \\) only <br>
\\(\rho ~= KSt\\) <br>

Sigma and time affect rho equally. 

#### Theory 6

Late game c5 term dominates. <br>

\\(\rho ~= Ac_5qr^2 \\) after integrating <br>
\\(\dot{r}, \dot{q} ~= A;  r, q ~= At\\) <br>
\\(\rho ~= KSt^3\\) <br>

Time affects rho 3 magnitude more than sigma.

#### Theory 7

Late game c6 term dominates. <br>

\\(\dot{\rho} ~= Ac_6\sqrt{\frac{\rho_2}{\rho_1}} \\) after partial differentiation <br>

However rho2 / rho1 is effectively constant. This is because if rho2 is higher than rho1, rho1 will eventually catch up to rho2 and vice versa. <br>

Therefore: \\(\dot{\rho} ~= Ac_6\\) <br>
\\(\rho ~= KSt\\) <br>

Sigma and time affect rho equally. 

#### Theory 8

The cost value scalings for c3, c4, c5 are the same. Since they are additive with each other, we can simplify the equation as: <br>

\\(\dot{\rho} ~= A\sqrt{Bc3}\\) <br>
\\(\dot{\rho} ~= A\\) <br>
\\(\rho ~= KSt \\) <br>

Sigma and time affect rho equally. 


From the equations above, we can conclude that for theories 1, 3, 5, 7, 8, rhodot and sigma are linearly dependent on each other. <br>
For theory 4, rhodot^1.5 is proportional to sigma. <br>
For theory 6, rhodot^3 is proportional to sigma. <br>
For theory 2, rhodot^10.2 is proportional to sigma. <br>

These conclusions imply that for theory 2 for example, increasing sigma hardly affects rhodot.


### Overpushing Coefficients

From previous workings, the overpushing coefficients are:

<table>
<tbody>
<tr>
    <td>T1 </td>
    <td>T2 </td>
    <td>T3 </td>
    <td>T4 </td>
    <td>T5 </td>
    <td>T6 </td>
    <td>T7 </td>
    <td>T8 </td>

</tr>
<tr>
    <td>1 </td>
    <td>10.2 </td>
    <td>1 </td>
    <td>1.5 </td>
    <td>1 </td>
    <td>3 </td>
    <td>1 </td>
    <td>1 </td>
</tr>
</tbody>

</table>

This means that for 'perfect' overpush, we should push the maximum of {T1, 10.2T2, T3, 1.5T4, T5, 3T6, T7, T8} where Tn are the taudots of each theory. This will maximize long term tau gain, assuming everything else is equal. 