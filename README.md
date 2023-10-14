Natural parallelism often presents itself in computational problems where individual tasks do not rely on others. This inherent parallel nature is frequently seen in the domain of image processing, where actions on pixels are mostly independent. This project delves into this nature by utilizing multiple parallel programming paradigms to efficiently process images.

The objective of this project is to expose different parallel programming languages and provide hands-on experience on how parallel programming operates in the context of image processing.

Within the submitted zip file, a folder project can be found, this will be our main project folder.
1. Navigate to the folder
2. Run `run.sh` or simply paste the below sequence of commands:
```
scancel -u { username } # to cancel submitted batch jobs
mkdir build
cd build
cmake ..
make - j4
cd ..
sbatch ./src/scripts/sbatch_PartA.sh
sbatch ./src/scripts/sbatch_PartB.sh
squeue # to check batch jobs queue
```
By default, the above commands will execute the RGB to Grayscale transformation for all provided images and the Image Filtering only for the *20K* image (the image is not available within this repository). If one wish to test other images, one can simply modify the appropriate scripts located in `src/scripts/` . Additional scripts for different images might also be found in the parent directory, `..` . Upon completion, one can find the experiment results in the directory: `images/results/` .
