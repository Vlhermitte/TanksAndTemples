# DISCONTINUATION OF PROJECT #  
This project will no longer be maintained by Intel.  
Intel has ceased development and contributions including, but not limited to, maintenance, bug fixes, new releases, or updates, to this project.  
Intel no longer accepts patches to this project.  
 If you have an ongoing need to use this project, are interested in independently developing it, or would like to maintain patches for the open source software community, please create your own fork of this project.  
  
# Tanks and Temples

This repository is used for discussing issues regarding the website that hosts the *Tanks and Temples* dataset.  
http://www.tanksandtemples.org

In order to evaluate your reconstruction algorithm on our benchmark, you need to download the dataset, reconstruct 3d geometry, submit your results, get evaluated, and be put on the leaderboard. Please follow the instructions on the website. If you encounter any problem, first check if the problem is listed on [FAQ](FAQ.md). If not, go to the [issues page](https://github.com/IntelVCL/TanksAndTemples/issues) to search if there is any duplicate of your problem. If not, file an issue and we will respond as fast as we can. Alternatively, you can send an email to [info.tanksandtemples@ivcl.org](mailto:info.tanksandtemples@ivcl.org).

## Python scripts

The [python_toolbox](python_toolbox) folder includes the python scripts for downloading the dataset and uploading reconstruction results. The python scripts are under the [MIT license](LICENSE). The dataset itself has a different license, see [this page](https://tanksandtemples.org/license/) for details.

Usage of downloader:
```
> python download_t2_dataset.py [-h] [-s] [--modality MODALITY] [--group GROUP] [--unpack_off] [--calc_md5_off]

Example 1: download all videos for intermediate and advanced scenes
> python download_t2_dataset.py --modality video --group both

Example 2: download image sets for intermediate scenes (quick start setting)
> python download_t2_dataset.py --modality image --group intermediate

Example 3: show the status of downloaded data
> python download_t2_dataset.py -s
```

Usage of uploader:
```
> python upload_t2_results.py [-h] [--group GROUP]

Example 1: upload intermediate and advanced reconstruction results
> python upload_t2_results.py --group both

Example 2: upload only intermediate results
> python upload_t2_results.py --group intermediate
```
