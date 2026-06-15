# Archived legacy repository

All legacy files and the full repository history are preserved in the branch `pre-cleanup-backup`.

If you need to recover any removed file, you can:

1. Check out the backup branch locally:

   git fetch origin
   git checkout -b restore-from-backup origin/pre-cleanup-backup

2. Copy any files you need from that branch into your cleaned branch.

This cleanup was performed to provide a clear, maintainable repository surface focusing on modern sentiment analysis for Amazon reviews. The full history remains available in `pre-cleanup-backup`.
