# squeaky
An updated pipeline for pan-genome investigation


### Pipeline

1. Run prodigal on full dataset (so as not to run into issue with its model inference step)
2. Order inferred gene sequences from largest to smallest
3. Cluster from largest to smallest using jackhmmer or mmseq2 (https://github.com/soedinglab/mmseqs2)
4. Classify resulting models using profile hmm vs profile hmm tool (https://github.com/soedinglab/hh-suite)
5. Alternatively generate the most likely sequence for each hmm model and classify using the prokka pipeline
6. Use capture-reacture methods that take into account measurement error (ghost records) http://www.math.canterbury.ac.nz/~r.vale/Mta.pdf
