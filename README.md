# Project E-shop
This repository contains the implementation of an **intelligently distributed application** of an electronic store (for instance: Amazon). The course ECSDI (Knowledge Engineering and Distributed Intelligent Systems) has been taken in 2020-Q2, spring season.

We have applied **agent-oriented programming** concepts to build this project. This means that we had to create an **ontology** for the program agents. This whole thing is related to the **Semantic Web** concept. We have used the **python** programming language, also **flask** framework to creat REST API easily and simulate agents behaivor. 

## Members of this project
- Alejandro, Kenny
- Clemente, Daniel
- Hossain, Tanvir

## Summary
[Read the statement](Statement.pdf)

Before start setup the environment and install 

    pipenv install
    pipenv shell
    pip install flask

We will use the Flask framework and REST services that allow us to create simple web APIs in order to represent and create agents so that they can make the functionalities of the app. Therefore, we will use REST as a gateway, that is, we will simulate the **methodology of multi-agent systems**.

By default the application starts up at the local address (127.0.0.1) and on port 5000, but we can configure it using the host and port parameters as follows app.run (host = "myweb.org", port = 9999)

Each agent (which will be a web app) will need to define a set of entry points to offer a service and the different REST operations (get, post, put, delete). An entry or route is defined with 
    
    @app.route ("url" {, methods = ["GET"]})

In our case, each port represents an agent, which acts as a Rest API since by its port we can receive requests from other agents so that they can perform one or more tasks of the application. This task or service must be associated with a resource that will have a defined URL address. 
      
> See: ECSDI_LAB/Examples/flask
#### Simple example of distribuited systems 
ECSDI_LAB/Examples/Distributed
In this exemples all are AGENTS that englobes SERVICES  
Two different ways to simulate a distribuited system: 
- **Open version resolution**: all agents are public in the directory service <br>
    DistributedSolverOpen <br>
    Infrastructure (DirectoryService ⇒ it simply takes care of registering all the services so that you can communicate)
    Frontend, Backend, Cliente 
- **closed resolution version**: now the specific resolvers are engaged with generic resolvers, they are not visible to other agents
    DistributedSolverClosed <br>
#### SimpleDirectoryAgent
It is important to execute as follows, otherwise it does not work ⇒ $ python 1_SimpleDirectoryService.py --open
This agent behaves as a platform so that the agents of the app can register in it and that they can work correctly. In each agent we have the comments.
#### Ontology
we have used the tool **protege 5** to creat an ontology or dictionary <br>
ECSDI_LAB/ontologías <br>
pip install ontodocs <br>
ontodocs fipa-acl.owl (to generate documentation)
## Additional Information
- this practice is not finished
>
    [packages]
    pip install flask
    pip install requests
    pip install rdflib
    pip install SPARQLWrapper
    pip install semantics3

>
    [necessary packages]
    multiprocessing
    flask
    flask-restful
    requests
    rdflib (library for ontologies and semantic web)
    sparqlwrapper