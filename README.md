# STAT 37787 Trustworthy Machine Learning Project
## Group member: Mengqi Liu, Yudan Tang

This repository stores the reimplementation of the result from the ICLR 2022 paper, ["Fairness Guarantees under Demographic Shift"](https://openreview.net/forum?id=wbPObLm6ueA), we hope to see the fairness of the algorithm proposed in this paper and see if the success in this algorithm is also reproducable in other datasets. 

# Installation

First, install Python 3.x, Numpy (1.16+), and Cython (0.29+).

The remaining dependencies can be installed by executing the following command from the Python directory of : 

	pip install -r requirements.txt

# Usage

The results of experiments from the paper are already stored in the path `Python/results/*`.

Meanwhile, those experiments can be re-executed by running the provided batch file from the Python directory, as follows:

     ./experiments/scripts/iclr_ds_experiments.bat

This command will run the experiments for Demographic Parity (dp), Disparate Impact (di), Equal Opportunity (eopp), Equalized Odds (eodd), and Predictive Equality (pe), and store the results as h5 files in `Python/results`. 
     
The figures we reproduced is stored in the path `Python/figures/*`. 

Meanwhile, once the experiments complete, the figures can alse be regenerated using the following two commands, 

     # for known distribution shift
     python -m experiments.scripts.iclr_figures_adult 
     # for unknown distribution shift
     python -m experiments.scripts.iclr_figures_adult --unknown_ds

This command will generate the result for the five concepts in fairness machine learning and generate the accuracy, the 
    
Once completed, the new figures will be saved to `Python/figures/*` by default.

# License

SeldonianML is released under the MIT license.


