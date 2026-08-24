#!/bin/bash

echo "===== Top CPU Consuming Processes ====="

ps aux --sort=-%cpu | head -10

echo ""
echo "===== Current CPU Usage ====="

top -b -n 1 | head -15
