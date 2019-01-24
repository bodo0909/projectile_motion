# projectile_motion

[![Build Status](https://travis-ci.org/bodo0909/projectile_motion.svg?branch=master)](https://travis-ci.org/bodo0909/projectile_motion)
[![Coverage Status](https://coveralls.io/repos/github/bodo0909/projectile_motion/badge.svg?branch=master)](https://coveralls.io/github/bodo0909/projectile_motion?branch=master)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/26c92bdb188b4db6adcaa775c0ec5d04)](https://www.codacy.com/app/bodo0909/projectile_motion?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=bodo0909/projectile_motion&amp;utm_campaign=Badge_Grade)

**Problem Statement**:
A projectile is launched from a known height and with a known speed, but the angle at which it is launched is unknown. The goal of this project is to determine how the uncertainty in the angle is propagated to the the uncertainty in the final launch distance, or the horizontal distance the projectile travels before hitting the ground.

![alt text](images/diagram.png)

The project will involve X phases, which are outlined below.

* Model Development
  * Create a model of the projectile's motion that takes a launch angle as input and returns a launch distance as output.
  * The model should be a Python class with a method called "evaluate" that takes in an input and returns an output.

* Model Evaluation Over a Grid of Inputs
  * Modify the model class or make another class that enables evaluation of the model over a grid of input angles that returns a corresponding grid of output values.

* Surrogate Model Development
  * While not the case for this example, computational models are often expensive in terms of the time required to generate an output for a given input parameter.
  * One way to combat this issue is to use machine learning algorithms to train what is called a surrogate model.
  * Using the scikit-learn Python package, create a surrogate model that is trained by results of your model class evaluated over a grid of launch angles.

* Monte Carlo Simulation
  * Assuming that the uncertainty in the launch angle can be captured by a Beta distribution with (NEED PARAMS), use Monte Carlo simulation to estimate the launch distance distribution using your original model (not the surrogate).
  * Time the simulation

* Surrogate-based Monte Carlo Simulation
  * Repeat the Monte Carlo simulation using the surrogate model.
  * Time the simulation, and compare with the original model Monte Carlo results.


**Prerequisites**:
* Install Python module dependencies: pip install -r requirements.txt

**Background Reading**:
* pytest
  * Testing your code
  * https://docs.pytest.org/en/latest/
  * https://semaphoreci.com/community/tutorials/testing-python-applications-with-pytest

* pylint 
  * Checking your coding style/cleaniless/standards 
  * https://docs.pylint.org/en/1.6.0/tutorial.html

* scikit-learn
  * https://scikit-learn.org/stable/documentation.html
  * A good flowchart for picking your machine learning algorithm: https://scikit-learn.org/stable/tutorial/machine_learning_map/index.html

* Monte Carlo Simulation
