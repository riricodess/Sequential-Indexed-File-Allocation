# Sequential-Indexed-File-Allocation

This repository contains C programs implementing Sequential and Indexed File Allocation for Operating Systems Experiment 14.

## Aim
To implement and compare sequential and indexed file allocation for `movie.mp4` on an online movie streaming server.

## Programs Included
- `seq.c` — Sequential file allocation program.
- `idx.c` — Indexed file allocation program.
- `seq_output.txt` — Sequential allocation output.
- `idx_output.txt` — Indexed allocation output.
- `seq_output.png` — Sequential allocation output image.
- `idx_output.png` — Indexed allocation output image.

## Requirements
- GCC compiler
- Linux terminal or Ubuntu environment

## Compilation and Execution

### Sequential Allocation

Compile and run the program:

```bash
gcc seq.c -o seq
./seq
```

### Indexed Allocation

Compile and run the program:

```bash
gcc idx.c -o idx
./idx
```

## Expected Output

### Sequential Allocation

```text
movie.mp4 start=20 length=5
block 0 -> disk block 20
block 1 -> disk block 21
block 2 -> disk block 22
block 3 -> disk block 23
block 4 -> disk block 24
```

### Indexed Allocation

```text
movie.mp4 index lookup
block 0 -> disk block 7
block 1 -> disk block 42
block 2 -> disk block 13
block 3 -> disk block 58
block 4 -> disk block 3
```

## Real-World Application
An online movie streaming server stores movie files on disk. Sequential allocation stores file blocks consecutively, while indexed allocation uses an index to locate blocks that may be scattered across the disk.

## Conclusion
Sequential allocation provides simple sequential access when consecutive disk blocks are available. Indexed allocation supports direct access and easier file growth, but requires an additional index block and may involve more disk-head movement.
