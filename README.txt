In this folders you can find two codes:

-general: here there is a programm made of a lot of classes and subclasses. In main.cpp you can choose which configuration you want
to use, the possibilities are:
*InitialCondition::twoBodyProblem()  --> it configures the solar system with just Sun and Earth with the Sun fixed at the center of the frame.   
*InitialCondition::threeBodyProblem()  -->  It configures the solar system with Sun, Earth and Jupiter with the Sun fixed at the center of the frame or with the CM fixed and the Sun free to move. To do this go inside three_body_problem.cpp and follow the instructions.
*InitialCondition::twoBodyRange()  --> it solves the task 3d of the project. 
*InitialCondition::tenBodyProblem()   --> It configures the solar system with all the planets plus Pluto with the Sun fixed at the center of the frame or with the CM fixed and the Sun free to move. To do this go inside ten_body_problem.cpp and follow the instructions.


To choose stepsize go to integral.h anche change m_dt
To choose number of steps go to initialconditions.cpp, and here you can choose the number of steps for each configuration. For example: twoBodySystem->integrate ("here");
Remember: number of years=number of steps X step size

-perihelion: it's the code specialized to solve last part of project (i.e. to find the angle at the first perihelion of Mercury with respect to the initial position after a century). It is made in this way to reduce as much as possible the computation time as we need a lot of precision.
However using (stepsize) h=1e-7 it needs 12 min; using h=0.5*e-7 it needs 20 min. 