# TensorFlow Optimizer of the Analytical Free Energy Model of Molecular Binding 

A class based on TensorFlow for the Maximum Likelihood optimization of the analytic model for the free energy of molecular binding.

## Contributors:

Denise Kilburg, dmkilburg@gmail.com

Emilio Gallicchio, egallicchio@brooklyn.cuny.edu

Solmaz Azimi, solmaz.azimi@brooklyn.cuny.edu

## References:

1. Denise Kilburg and Emilio Gallicchio. Analytical Model of the Free Energy of Alchemical Molecular Binding. J. Chem. Theory Comput. 14, 6183–6196 (2018) [doi:10.1021/acs.jctc.8b00967](http://dx.doi.org/10.1021/acs.jctc.8b00967) [pdf of submitted manuscript](https://www.dropbox.com/s/td1mlagbbg0siqp/analytical_theory_ms4.pdf?dl=0)

## Examples

From [Alchemical Transformations for Single-Step Hydration Free Energy Calculations. arXiv:2005.06504 (2020)](https://arxiv.org/abs/2005.06504)


## To employ with the most recent version of AToM
#### Leg is specified as either 1 or 2
#### For inspection instead of lambda state, designate stateID

Usage:

```
python femodel_tf_optimizer-linear_AToM.py -o -l 1 -d data/h2o_explicit_AToM.dat
```

Inspection:

```
python femodel_tf_optimizer-linear_AToM.py -r -l 1 -s 10 -d data/h2o_explicit_AToM.dat
```

Restart Optimization:
```
python femodel_tf_optimizer-linear_AToM.py -r -o -n 1000 -l 1 -d data/h2o_explicit_AToM.dat
```

### Hydration of 1-naphthol (linear alchemical potential)

Usage:

```
python femodel_tf_optimizer-linear-example.py -h
```

Inspection:

```
python femodel_tf_optimizer-linear-example.py -l 0.267 -d data/water-droplet-1-naphthol-linear/repl.cycle.potE.temp.lambda.ebind.lambda1.lambda2.alpha.u0.w0.dat
```

Optimization:

```
python femodel_tf_optimizer-linear-example.py -o -c 10 -n 10 -d data/water-droplet-1-naphthol-linear/repl.cycle.potE.temp.lambda.ebind.lambda1.lambda2.alpha.u0.w0.dat
```

Restart optimization:

```
python femodel_tf_optimizer-linear-example.py -r -o -c 10 -n 10 -d data/water-droplet-1-naphthol-linear/repl.cycle.potE.temp.lambda.ebind.lambda1.lambda2.alpha.u0.w0.dat
```


### Hydration of 1-naphthol (integrated logistic alchemical potential)

Usage:

```
python femodel_tf_optimizer-ilog-example.py -h
```

Inspection:

```
python femodel_tf_optimizer-ilog-example.py -l 0.267 -d data/water-droplet-1-naphthol-ilog/repl.cycle.potE.temp.lambda.ebind.lambda1.lambda2.alpha.u0.w0.dat
```

Optimization:

```
python femodel_tf_optimizer-ilog-example.py -o -c 10 -n 10 -d data/water-droplet-1-naphthol-ilog/repl.cycle.potE.temp.lambda.ebind.lambda1.lambda2.alpha.u0.w0.dat
```



