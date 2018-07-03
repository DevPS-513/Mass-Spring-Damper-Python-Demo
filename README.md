# Mass-Spring-Damper-Python-Demo
Solves for the response of a Damped mass and spring system under a sinusoidal  input, the example it solves can be found
at  https://www.crcpress.com/downloads/K11527/MATLAB%20Resources.pdf


System mode: Mass connected to rigid ground via a spring and damper, a force input is fo*sin(wt)


Turning this into state space gives 
q_dot= Aq+Bu
y=Cq+Du

k = 100*newtons/meters
m = 1*kg
damping_ratio = 0.1
omega_n = np.sqrt(k/m)
c = zeta*2*np.sqrt(m*k)

A = [[0, 1], [-k/m, -c/m]]
B = [[0], [1]]
C = [[1, 0]]         This will chose displacement as our output
D = 0
