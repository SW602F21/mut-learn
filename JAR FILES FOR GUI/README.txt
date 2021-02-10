-------------------------------------
Genetic Programming of Timed Automata
-------------------------------------
System requirements:
--------------------
The graphical user interface (GUI) demonstrating genetic programming (GP) of 
timed automata requires version 8 of the Java runtime environment. Other than 
that, there are no known limitations or requirements. The application may use a 
large amount of memory, though. If popuplation sizes greater than 1000 are used, 
the available heap memory should be at least 2GB and preferably more than 4GB 
(use -Xmx command line option for JVM).

Quick Guide:
------------
* Overview:
  The GUI consists of three tabs: one for settings, another one to display
  the evolution of the population of timed automata, and one tab for displaying
  the original timed automaton that generates the timed traces used as basis for
  GP (in the demonstrator, the original automaton is known, but it is treaded as
  a black box for GP).
* Choosing an experiment:
  One of 44 different experiments can be chosen via the dropdown menu in the 
  upper left corner. These are timed systems which are executed with simulated 
  time in the testing phase.
* Parameter settings:
  The parameters discussed in the paper can be entered in the corresponding text
  fields.
* Performing an experiment:
  Experiments are started using the "Start Evolution" button in the lower left
  corner of the first tab. They are stopped by pressing the button on the
  opposite side or once the experiment is finished.
  As soon as an experiment is started, a progress bar shows the progress of the 
  current experiment. If it is full, we reached the maximum number of 
  generations. 
* Exploring search progress:
** A tree view in the second tab allows exploring the search. We store the 
   selected best individuals of all generations. 
** Examining an individual:
   If an individual is selected in the tree view (if a generation is selected
   we show the best individual of the generation), we show the corresponding 
   timed automaton in the middle and some fitness-relevant data on the 
   right-hand side. 
** Zooming: Individuals may be quite large. After clicking on a timed automaton,
   it can be zoomed by holding the shift-key and scrolling the mouse wheel.
* Original timed automaton:
** The third tab shows the original timed automaton for the currently chosen 
   experiment. That is, we show the timed automaton, which we are trying to 
   learn. Note that we do not know this automaton in general, but we know the 
   original timed automaton for the experiments.

Additional functions:
---------------------
** Test data:
   We store test data for all tests and all individuals. It allows users to 
   to explore passed/failed tests. Tests are also accessible via the tree view
   and once a test is selected, the corresponding timed trace of the SUT will be
   displayed at the bottom of the GUI
** Navigation buttons:
*** Next Best: If an indidivual is selected, the button will select the best 
    individual of the lowest generation with a better individual (if possible)
*** Best Overall: Selects the best individual found so far
*** Animate: If toggled, it selects the next best individual in certain time 
    intervals where the length of the intervals is given by the slider below.
** Export: 
   If an individual is selected it can be exported in SVG format via a button on
   the right-hand side.
