=========
PythonPSO
=========
Short and sweet particle swarm optimization implementation in python

Requirements
------------
-python 3
 numpy

Example Usage
-------------
Minimize function: ::

    def simple_error_function(args):
        return args[0]+args[1]

    number_of_parameters = 2
    max_iterations = 100
    best_parameters, best_error_score = particle_swarm_optimize(simple_error_function,
                                            number_of_parameters, max_iterations)

returns the best found parameters and it's score for that function

Custom parameter weight initalization: ::
    def simple_error_function(args):
        return args[0]+args[1]

    def parameter_init():
        return random.random()*0.5-10

    number_of_parameters = 2
    max_iterations = 100
    best_parameters, best_error_score = particle_swarm_optimize(simple_error_function, number_of_parameters,
                                            max_iterations, weight_init, parameter_init=parameter_init
                                            #other arguments
                                            stopping_error=0.0001,#stop when we have a particle with this score
                                            num_particles=10, #number of particles to run
                                            max_iterations_without_improvement=10,#stop when we have this many consecutive turns without improvement
                                            c1: float=2.0,
                                            c2: float=2.0)