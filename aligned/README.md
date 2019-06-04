Aligned FASTQ files obtained using the code at https://github.com/shubhamchandak94/LDPC_DNA_storage/blob/master/util/align_compute_stats.sh, compressed using [SPRING](https://github.com/shubhamchandak94/Spring/). To decompress, download and install SPRING and run
```
for i in {1..9}; do
  ./spring -d -i exp_aligned_$i.fastq.spring -o exp_aligned_$i.fastq
done
```

To extract the reads from the FASTQ files (read file needed for decoding), run
```
for i in {1..9}; do
  sed -n '2~4p' exp_aligned_$i.fastq > exp_aligned_$i.reads 
done
```
