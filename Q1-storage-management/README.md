#!/bin/bash

echo "===== Disk Usage ====="
df -h

echo ""
echo "===== Log Directory Usage ====="
du -sh /var/log

echo ""
echo "===== Largest Log Files ====="
du -ah /var/log 2>/dev/null | sort -rh | head -10

echo ""
echo "===== Log Rotation Status ====="
systemctl status logrotate.timer --no-pager
