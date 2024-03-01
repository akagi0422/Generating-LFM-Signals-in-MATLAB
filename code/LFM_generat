%% ——LFM——

clc;
clear;
close all;

%% ——造LFM——

% 参数设置
T = ;    % 信号持续时间（秒）
F_start = ;
F_end = ;
B = F_end - F_start;   % 频带宽度
Fs = ;  % 采样率
K = B / T;    % 调制斜率

% 生成时间向量
N_LFM = round(T / (1 / Fs));  % 根据采样率计算采样点数
t_LFM = linspace(0, T, N_LFM);  % 在持续时间范围内生成均匀分布的时间向量,单边LFM从0到T
% 相当于 t = (1:N)*1/Fs; % 长度为1到N，频率为Fs生成时间序列
% t = linspace(-T/2, T/2, N); % 双边LFM用这个

% 生成LFM信号
st = (abs(t_LFM) < T) .* exp(1j * pi * K * t_LFM.^2); % 本地参考信号
% st = (abs(t) < T/2) .* exp(1j * pi * K * t.^2); % 双边LFM用这个
