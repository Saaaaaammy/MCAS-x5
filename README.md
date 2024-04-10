# MCAS-x5
X5
LE2038: Design of an aircraft pitch controller QUB, 2023/24
Group Assignment
Important: Before you start, read the instructions
1 Problem statement
You need to design a control system for the pitch of an aircraft. The system is illustrated in Figure 1.
The manipulated input is the elevator deflection angle, δ; changing the deflection rate affects the pitch
of the aircraft. In Figure 1 α denotes the angle of attack, which is the angle between the longitudinal
axis of the aircraft and its velocity vector. The pitch angle of the aircraft is denoted by θ. The pitch
rate is denoted by r.
Figure 1: Illustration of an aircraft with its pitch angle, θ, the angle of attack, α, and the deflection
angle of the elevators, δ. The angle γ = θ − α is known as the slope.
The system dynamics is described by the following system of differential equations
 ̇α = − 0.31α + 56.7r + 0.231δ, (1a)
 ̇r = − 0.014α − 0.426r + 0.0203δ, (1b)
 ̇θ = 56.7r, (1c)
where all quantities are in SI units1. In addition, the deflection angle of the elevators is controlled
by an actuator whose dynamics has been found to be of the first order with unit static gain and a
time constant of 10 ms. The sensor has the transfer function Gm(s) = exp(−0.005s), i.e., the sensor
introduces a delay of 5 ms.
1In Equation (1), α, θ and, δ are measured in radians — not degrees — and q is measured in radians per second.
1
2 ELE8088
The task of your team is to:
1. Present a complete analysis of the given dynamics: Your report should include a detailed
study of the properties of the open-loop dynamics and your results should be accompanied by
appropriate plots.
2. Design an appropriate controller for the system: Your controller needs to satisfy the stan-
dard requirements for a closed-loop control system. You need to make sure that the controlled
system is BIBO-stable and that there is zero offset. Additionally, you may want to check how
your closed-loop system will behave in presence of disturbances. You need to consider what sort
of possible disturbances may be present. You should tune your controller to achieve reasonable
stability margins and of course to exhibit a desirable (not highly oscillatory, not overly slow, not
too aggressive) closed-loop behaviour.
You may use any part of the theory from the textbook. You can also use Python for your calculations
and for plotting, but you will need to include a link to your code.
Here is a hint to get you started: Assuming zero initial conditions, apply the Laplace transform to
each of the equations in (1). Then determine the transfer function of the system with the input being
deflection angle of the elevators and the output being the pitch angle.
2 Marking
Your report will be marked for technical correctness and completeness of the proposed approach, jus-
tification, clarity, quality of presentation; this will account for 90% of the marks of your report. Your
report must include an appendix or section entitled “project management and individual contribu-
tions” where you should provide evidence on (i) how you collaborated (what collaboration tools did
you use? For example, did you use git/GitHub?) (ii) how you managed the work in this project? How
were the tasks distributed? Did you use an issue tracker? (iii) any additional information project man-
agement you would like to include (e.g., planning), (iv) what were the contributions of each member
of the team?
As mentioned in the previous paragraph, your report will be marked for its quality of presentation.
To get a good mark, I would encourage you go through the slides on “how to write a good technical
report.”
Marks will only be awarded based on the evidence you will provide. Examples of appropriate evi-
dence can be meeting minutes, or a link to a GitHub repository, or other similar online collaborative
development space. This will account for 10% of the marks of your report
