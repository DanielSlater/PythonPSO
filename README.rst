Particle swarm optimization implementation in python
=======================

Requirements
----
python 3
numpy

Example Usage
----
.. code-block:: Python
    def simple_error_function(args):
        return args[0]+args[1]

    number_of_parameters = 2
    max_iterations = 100
    result, best = particle_swarm_optimize(simple_error_function, number_of_parameters, max_iterations)