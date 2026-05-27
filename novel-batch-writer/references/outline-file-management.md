# Outline File Management Lessons

## The One-Batch-One-File Rule

Each 5-chapter batch uses exactly one file with its exact chapter range:
- Correct: `5-第136-140章-分章大纲.txt`
- Wrong: `5-第136-150章-分章大纲.txt` (covers 3 batches, overlaps)

## Why This Matters

When Part B starts, it checks for `5-第{N}-{N+4}章-分章大纲.txt`. Overlapping files cause confusion.

## Cleanup Procedure

Before writing a new batch file:
1. Check if any existing file overlaps the new batch's range
2. If yes, DELETE the overlapping combined file

## Cross-Volume Cleanup

When switching volumes, remove old volume's combined files and overlapping files.
