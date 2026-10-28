# soil-infiltration-models
Soil water infiltration modeling using MATLAB
clc;
clear;
close all;

% Example: Horton infiltration model

f0 = 50;    % Initial infiltration rate
fc = 10;    % Final infiltration rate
k  = 0.5;   % Decay coefficient

t = 0:1:10; % Time

f = fc + (f0 - fc) .* exp(-k .* t);

plot(t, f, 'b-o', 'LineWidth', 1.5);
xlabel('Time');
ylabel('Infiltration rate');
title('Horton Infiltration Model');
grid on;
