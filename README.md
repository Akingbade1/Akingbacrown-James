# Epidemiological Modelling Projects

This repository contains code developed for research in infectious disease modelling, including:

- Avian Tuberculosis (Avian-TB)
- Typhoid Fever models
- Deterministic compartmental models
- Preliminary stochastic modelling extensions

Tools used:
- MATLAB
- Python

The work focuses on understanding disease transmission dynamics and evaluating intervention strategies using mathematical modelling approaches.

function dy = modelodeRungeKutta_order4withoutcontrol
% Parameters
wedge = 140; betah = 0.3425; betap = 0.002; mu = 0.07; psi = 0.34;
tau2 = 0.3; tau3 = 0.20; epsilonp = 0.8; alpha2 = 0.002; alpha3 = 0.004;
delta2 = 0.1; delta6 = 0.001; sigmah = 1.0; sigmap = 0.38; a2 = 0.59; a3 = 0.31;
gammap = 0.23; gammah = 0.01; phi2 = 1.0; gammaph = 0.5; pi =0.2; eta1 =0.3;
eta5 = 0.6; eta7 = 0.2; N = 2000;

% Runge-Kutta parameters
M = 1000; Tmax = 30; h = Tmax/M; h2 = h/2; h6 = h/6;
t = linspace(0, Tmax, M+1);

% Preallocate compartments
S = zeros(1,M+1); V = zeros(1,M+1); Eh = zeros(1,M+1); Ep = zeros(1,M+1);
Jp = zeros(1,M+1); Jh = zeros(1,M+1); Ip = zeros(1,M+1); Ih = zeros(1,M+1);
Iph = zeros(1,M+1); T_comp = zeros(1,M+1); Rp = zeros(1,M+1);

% Initial conditions
S(1) = 2550; V(1) = 500; Eh(1) = 400; Ep(1) = 400; Jp(1) = 400; Jh(1) = 400;
Ip(1) = 10; Ih(1) = 400; Iph(1)= 15; T_comp(1) = 10; Rp(1) = 1;

% Loop over time
for i = 1:M
    % Compute Runge-Kutta 4 steps here
    % Use the same logic you wrote, but replace T(i) -> T_comp(i)
    % At the end, update S(i+1), V(i+1), ..., T_comp(i+1)
end

% Output
dy = [t; S; V; Eh; Ep; Jp; Jh; Ip; Ih; Iph; T_comp; Rp];

% Optional plotting
figure; plot(t, Ih, '-', 'LineWidth', 2)
xlabel('Time (days)'); ylabel('Infected Ih(t)');
end
