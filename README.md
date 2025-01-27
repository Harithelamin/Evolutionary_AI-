# Evolutionary_AI
Solving tasks in OpenAI Gym

 
#Background  
One  popular  way  of  evaluating  AI  algorithms  is OpenAI Gym. OpenAI Gym  is  a  collection  of 
environments in  many  different  domains,  ranging  from  simple  Atari  video  games  to  more 
complex robot control environments. It offers an easy to access, standardized set 
of environments currently used in state-of-the-art AI research and development. While they 
provide the environments, the users provide the AI algorithm to be tested and evaluated.   
 
#Aim  
In this group project topic, you will implement a control system using some of the complex 
systems  models  studied  in  the  course,  such  as a  cellular  automaton  and  an  artificial  neural 
network. This control system will maintain a pole balanced upright on a cart by moving left or 
right.  The  selected  control  system  will  evolve  to  learn  this  task  by  using  evolutionary 
algorithms. This cart-pole balancing environment is part of the OpenAI Gym library. You can 
find more information about it on this 
link: https://www.gymlibrary.dev/environments/classic_control/cart_pole/. 
  
 
#Tasks  
The overall progress of the project should be an iterative exploration of different models and 
optionally  fitness  functions,  with  each  iteration  giving  more  insight  into  what  improves  the 
behavior  of  the  controller  in  the  given  environment.  As  you  work  on  this  project,  keep  the 
following questions in mind. What does the fitness function tell me about the environment? 
How does the behavior of the controllers change from generation to generation as I 
evolve them? How do different parameter choices affect the outcome of the evolution? How 
are  the  outputs  from  the  environment  communicated  to  the  controller  and  how  are  the 
outputs from the controller decoded?  
  
To get started, follow this basic approach:  
1. Familiarize yourself with the models (CA and networks)  
2. Implement in Python a cellular automaton which receives arguments to define its rule  
3. Run  the  cart-pole  balancing  environment  using  random  actions.  You  can  install  and 
prepare this environment by following the instructions on this 
link: https://www.gymlibrary.dev/content/basic_usage/ 
4. Come up with a method to convert the environment state or observations into binary 
numbers. Thus, these numbers can be used as input or initial state of the cellular 
automaton  
5. Implement  a  random  generator  of  rule  arguments.  The  generated  arguments  are 
going to be passed to the cellular automaton to define its rule  
6. The initial state of the cellular automaton is defined by the environment observations 
as binary numbers. Come up with the input arrangement of these binary 
numbers into the CA  
7. Select and implement a method to determine the action of the cart. One suggestion is 
through majority voting system. It determines the action using the cells’ states with larger 
amount. For example, if there are more cells with state zero than with state one, then the 
cart moves left, otherwise the cart moves right  
8. Come  up  with a  fitness  function that  tracks  the  performance  of  the  cart  during  the 
entire environment simulation. You can use the rewards and environment 
observations that the function “step” returns  
9. Execution of the solution search:  
1. Generate random arguments to define the CA’s rule  
2. Make the  first observation of a  fresh (reset) environment. Transfer it into 
the CA as its initial state. It must follow the predefined input arrangement  
3. Execute a chosen number of time steps  
4. The current state of the CA is used to define its action according to a selected 
method  
5. Update  the  state  of  the  CA  according  to  the  new environment observation 
after the cart’s action  
6. Go to step 9.3 again until the environment simulation is done   
7. When simulation is done, apply the fitness function to determine the 
controller’s fitness score. Save the score and the CA’s rule applied  
8. Go to step 9.1 again until the stop condition of your search is reached  
10. After the solution search, rank your rules by the best fitness scores  
11. The previous steps perform a random search. Then, it can be improved to an 
evolutionary algorithm  
12. Expand your CA or to a network model (a simple neural network model). 
Then, evolve its parameters to improve the controller.  




#Resources   
• K.L. Downing, Intelligence Emerging, Chapters 6 and 7   
• Unsupervised learning of digit recognition using spike-timing-dependent plasticity. 
Diehl & Cook (2015) Front. Comput. Neurosci.  
https://www.frontiersin.org/articles/10.3389/fncom.2015.00099/full 
• Supervised learning in spiking neural networks: A review of algorithms and 
evaluations. Wang, Lin, & Dang (2020) Neural Networks 
https://www.sciencedirect.com/science/article/pii/S0893608020300563 
• http://yann.lecun.com/exdb/mnist/ (see papers with code link below if issues) 
• https://paperswithcode.com/dataset/mnist (see the section on Dataset loaders) 
• https://www.nengo.ai/ 
• https://snntorch.readthedocs.io/en/latest/tutorials/index.html 
