# Log Monitoring and Analysis Script

## Overview
This script is designed to monitor a log file (`/var/log/auth.log` by default) and perform basic analysis on the log entries. The analysis includes counting occurrences of specific keywords or patterns such as error messages and HTTP status codes.

## Functions
1. **monitor_log()**
   - Monitors the log file in real-time using `tail -f`.
   - Detects and displays new log entries as they appear.

2. **count_keywords()**
   - Counts occurrences of error messages and HTTP status codes in each log entry.
   - Utilizes `grep -o` to match whole words containing the specified keywords.
   - Updates and maintains total counts for error messages and HTTP status codes.

3. **sigint_handler()**
   - Handles interruptions (e.g., Ctrl+C) during log monitoring.
   - Triggers the generation of a summary report before exiting.

4. **generate_summary_report()**
   - Generates a summary report at the end of log monitoring or upon interruption.
   - Includes total log entries observed, total occurrences of error messages, and total occurrences of HTTP status codes.

## Usage and Testing
### Prerequisites
- Bash shell environment.
- Access to the log file being monitored (default: `/var/log/auth.log`).

### How to Use
1. Clone or download the script file (`log_monitor.sh`) to your local system.
2. Optionally, modify the log file path or keywords (error messages, HTTP status codes) in the script according to your requirements.
3. Open a terminal and navigate to the directory containing the script.
4. Run the script using `./log_monitor.sh`.

### Testing
- Start the script to begin monitoring the log file.
- Generate some log entries containing the specified keywords (error messages, HTTP status codes) to observe the counts in real-time.
- Interrupt the script (e.g., press Ctrl+C) to trigger the generation of the summary report.
- Review the summary report to see the total log entries observed and the counts of error messages and HTTP status codes.
