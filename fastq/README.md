Original FASTQ files obtained from the sequencer, compressed using [SPRING](https://github.com/shubhamchandak94/Spring/). To decompress, download and install SPRING and run
```
./spring -d -i exp_1.fastq.spring -o exp_1.fastq
./spring -d -i exp_2.fastq.spring -o exp_2.fastq
./spring -d -i exp_3-9.fastq.spring -o exp_3-9.fastq
```

To extract the reads from the first FASTQ file (read file needed for decoding), run
```
sed -n '2~4p' exp_1.fastq > exp_1.reads 
```
