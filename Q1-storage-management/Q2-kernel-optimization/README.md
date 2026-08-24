#!/bin/bash

echo "===== CPU Information ====="
nproc

echo ""
echo "===== Scheduler Information ====="
cat /proc/sys/kernel/sched_rr_timeslice_ms

echo ""
echo "===== Running Processes ====="
ps -eo pid,ppid,ni,pri,pcpu,comm --sort=-pcpu | head -10

echo ""
echo "===== Context Switching ====="
vmstat 1 3

echo ""
echo "===== Loaded Kernel Modules ====="
lsmod | head -10
