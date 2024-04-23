# Log Monitor Script

## Overview
This script monitors a specified log file in real-time and displays new log entries as they appear. It also generates a summary report upon exiting.

## Code Explanation

### Functions:

1. `monitor_log()`
   - Monitors the specified log file in real-time and displays new log entries.

2. `sigint_handler()`
   - Handles the SIGINT signal (Ctrl + C) to exit the log monitoring and generate a summary report.

3. `generate_summary_report()`
   - Generates a summary report that includes the total number of log entries.

4. `main()`
   - The main function that initiates the log monitoring process.

5. `trap`
   - Traps the SIGINT signal and directs it to the `sigint_handler()` function for graceful exit.


## Prerequisites
- This script requires a Unix-like environment with Bash installed.
- Ensure that you have permission to access the log file specified in the script.

## Usage
1. **Download the Script**: Download the `log_monitor.sh` script to your desired location.

2. **Set Log File Path**: Open the script in a text editor and update the `log_file` variable with the path to the log file you want to monitor.

3. **Run the Script**:
    ```bash
    bash log_monitor.sh
    ```

4. **Monitor Logs**:
   - Once the script is running, it will continuously monitor the specified log file.
   - New log entries will be displayed in real-time, showing the timestamp and the content of each entry.

5. **Exit Monitoring**:
   - To stop monitoring, press `Ctrl + C`.
   - This will trigger the generation of a summary report that includes the total number of log entries.

## Testing
To test the script:
1. Create a test log file (`test.log`) with some sample log entries.
2. Update the `log_file` variable in the script to point to `test.log`.
3. Run the script and add new entries to `test.log`.
4. Observe how the script displays new log entries in real-time.
5. Exit the script with `Ctrl + C` to see the summary report.
