# PINN Elasticity Imaging

## Repository Information

This repository is a mirror of the original codebase developed for the paper "Elasticity imaging using physics-informed neural networks: Spatial discovery of elastic modulus and Poisson's ratio" published in Acta Biomaterialia (2023).

**Original Repository:** https://github.com/klaksari/2D_hidden_elasticity_PINN

**Paper Details:**
- Title: Elasticity imaging using physics-informed neural networks: Spatial discovery of elastic modulus and Poisson's ratio
- Authors: Ali Kamali*, Mohammad Sarabian*, Kaveh Laksari
- Journal: Acta Biomaterialia
- Volume: 155
- Pages: 400-409
- Year: 2023
- DOI: https://doi.org/10.1016/j.actbio.2022.11.024
- *These authors contributed equally as co-first authors.

The code contained here demonstrates the work conducted in physics-informed neural networks for elasticity imaging as a first co-author of this paper.

For any questions or further information about this research, please refer to the published paper or contact the authors directly.


# Elasticity Imaging Using Physics-Informed Neural Networks: Spatial Discovery of Elastic Modulus and Poisson's Ratio
Data and codes from our 2022 paper: 
[Elasticity Imaging Using Physics-Informed Neural Networks: Spatial Discovery of Elastic Modulus and Poisson's Ratio](https://www.sciencedirect.com/science/article/pii/S1742706122007516)


In this study, we leveraged the power of neural networks as universal function approximators to estimate the spatial distribution of elastic modulus and Poisson's ratio using available data from elasticity imaging.
Our work is the first implementation of PINN that successfully discovers the spatial distribution of both materials parameters that fully define linear isotropic elasticity.
This repository currently contains data and sample code from loading of a domain with embedded stiff inclusion and the PINN implementation.
![image](https://user-images.githubusercontent.com/60515966/200451633-49d1b7e4-af03-4773-be5c-e583030db498.png)

## Quick Setup

install [SCiANN](https://www.sciann.com/) on a PC or virtual machine using:

```
pip install sciann
```
## Running the PINN code
Clone this repository and navigate to the Embedded_Inclusion_PlaneStress directory. Running the parameter discovery code could be done using the following function
for a batch size of 1024, 200,000 training epochs:

```
python PE_PINN.py -bs 1024 -e 200000
```

The code takes in 1D txt files containing x and y collocation points and strain terms as input and returns distributions of Young's modulus, Poisson's ratio, and stress at those coordinates.


## Plotting
One can use the included helper function to plot unstructured data over a structured grid given desired number of points on the x axis
```
python Plot_PE_PINN_Results.py -nxp 50
```

Sample input and output files for a 200,000-epoch run on coarse resolution are included as sample data.
Have a question about implementing the code? contact us at [klaksari@arizona.edu](mailto:klaksari@arizona.edu), [akamali@arizona.edu](mailto:akamali@arizona.edu), [ms322615@ohio.edu](mailto:ms322615@ohio.edu)
