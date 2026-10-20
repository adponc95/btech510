# Title: Lab6 Reproducible
- Author: Adrian Ponce
- Date: 10/19

This is my first markdown notebook.

I can make a numbered list:
1. Apple
2. Banana
3. Grapes

## Level 2 heading
I can make an unnumbered list
- NFL
- NBA
- MLB

### Level3 heading
I can also make a table
| col1         | col2          | col3        |
| ------------ | ------------- | ----------- |
| DNA          | RNA           | Protein     |
| Genetic code | Transcripts   | Peptide     |
| Double Helix | Single strand | Alpha helix |

### Code block with Python3 example with biopython >= 1.82
```python
#!/usr/bin/python3
import sys
from Bio import SeqIO
from Bio.SeqUtils import gc_fraction

def parse_fasta_file(fasta_file_path):
    sequences = SeqIO.parse(fasta_file_path, "fasta")
    for seq_record in sequences:
        print(seq_record.id, len(seq_record), round(gc_fraction(seq_record.seq), 2))

if __name__ == "__main__":
    parse_fasta_file(sys.argv[1])
