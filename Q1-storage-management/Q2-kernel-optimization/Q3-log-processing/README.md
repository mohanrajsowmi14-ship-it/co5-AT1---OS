#!/bin/bash

LOGFILE="access.log"
OUTPUT="result.txt"

echo "Processing log file..."

time awk '{print $1}' "$LOGFILE" | \
sort | \
uniq -c | \
sort -nr > "$OUTPUT"

echo "Processing completed."
echo "Output saved to $OUTPUT"
