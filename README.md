# Welcome to Search Engineering

Search Engineering is a four week class taught by Grant Ingersoll and Dave Anderson and is focused on helping students
quickly get up to speed on search best practices related to performance, scaling, fault tolerance, backups and recovery.  

Students will first learn to optimize a single node of search and then scale it out to a multi-node cluster.

The class is a hands-on project-driven course where students will work with real data and the [Opensearch](https://opensearch.com)/Elasticsearch ecosystem.

# Class code layout (e.g. where the projects are)

For our class, we have four weekly projects.  Each project
is a standalone Python application that interacts with an OpenSearch server (and perhaps other services).  

You will find these four projects in the directories below them organized in the following way:

- Week 1:
    - week1 -- The unfinished template for the week's project, annotated with instructions.
- Week 2:
    - week2 -- The unfinished template for the week's project, annotated with instructions.
- Week 3 and 4: you get the picture

Our instructor annotated results for each project will be provided during the class.  Please note, these represent our way of doing the assignment and may differ from your results, as there is often more than one way of doing things in search.

You will also find several supporting directories and files for Docker and Gitpod.

# Prerequisites

1. No prior search knowledge is required, but you should be able to code in Python or Java (all examples are in Python)
1. You will need a [Gitpod](https://gitpod.io) account.

# Working in Gitpod (Officially Supported)

*NOTE*: The Gitpod free tier comes with 50 hours of use per month.  We expect our work will be done in less time than that.  However, you may wish to conserve time on the platform by being sure to stop your workspace when you are done with it.  Gitpod will time you out (don't worry, your work will be saved), but that may take longer to detect.

The following things must be done each time you create a new Gitpod Workspace (unfortunately, we can't automate this)

1. Fork this repository.
1. Launch a new Gitpod workspace based on this repository.  
    1. Note: it can take a few minutes for OpenSearch and the dashboards to launch.
1. [TBD START WHATEVER APPROPRIATE OPENSEARCH]
1. You should now have a running Opensearch instance (port 9200) and a running Opensearch Dashboards instance (port 5601)
1. Login to the dashboards at `https://5601-<$GITPOD_URL>/` with default username `admin` and password `admin`. This should popup automatically as a new tab, unless you have blocked popups.  Also note, that in the real world, you would change your password.  Since these ports are blocked if you aren't logged into Gitpod, it's OK.

        $GITPOD_URL is a placeholder for your ephemeral Gitpod host name, e.g. silver-grasshopper-8czadqyn.ws-us25.gitpod.io

# Exploring the OpenSearch Sample Dashboards and Data

1. Login to OpenSearch and point your browser at `https://5601-<$GITPOD_URL>/app/opensearch_dashboards_overview#/`
1. Click the "Add sample data" link
1. Click the "Add Data" link for any of the 3 projects listed. In the class, we chose the "Sample flight data", but any of the three are fine for exploration.

# Running the Weekly Project

At the command line, do the following steps to run the example.  

1. Activate your Python Virtual Environment.  We use `pyenv` (Pyenv website)[https://github.com/pyenv/pyenv] and `pyenv-virtualenv` (Pyenv Virtualenv)[https://github.com/pyenv/pyenv-virtualenv].
    1. `pyenv activate search_eng` -- Activate the Virtualenv. 
1. Optional: You can run `ipython` if you like.
    
# Working locally (Not supported, but may work for you. YMMV)

To run locally, you will need a few things:

1. [Pyenv](https://github.com/pyenv/pyenv) and [Pyenv-Virtualenv](https://github.com/pyenv/pyenv-virtualenv) with Python 3.9.7 installed
1. [Docker](https://docker.com/)
1. A [Git](https://git-scm.com/) client

Note: these have only been tested on a Mac running OS 12.2.1.  YMMV.  Much of what you will need to do will be similar to what's in `.gitpod.Dockerfile`

1. `pyenv install 3.10.6`
1. `pip install` all of the libraries you see in `.gitpod.Dockerfile`
1. Setup your weekly python environments per the "Weekly Project" above.
1. Install [Fasttext](https://fasttext.cc/)  
1. Run OpenSearch: 
    1. `cd docker`
    1. `docker-compose up`
1. Do your work per the Weekly Project     
    