# PowerShell-Integrity-FIM

Overview

This PowerShell script is a simple File Integrity Monitor (FIM) that helps track changes to files and directories on your system. It can create a baseline of file hashes and monitor files for any unauthorized changes or deletions.

Features

1. Collect New Baseline: Generates hash values for target files and stores them in a baseline file (baseline.txt).
2. Monitor Files with Saved Baseline: Continuously monitors files, compares their current hash values to the baseline, and notifies the user if any files have been changed or deleted.

How It Works

1. Collecting a Baseline
2. The script calculates a SHA256 hash value for each file in the specified directory.
3. It stores the file path and corresponding hash value as pairs in a baseline file (baseline.txt).

Monitoring Files

1. The script loads the file-hash pairs from the baseline file (baseline.txt).
2. It continuously monitors the files in the baseline, recalculating their hash values and comparing them to the baseline.
3. If a file's hash value differs from the baseline, or if a file is deleted, the script notifies the user.
