Computer Science 61A

# How to set up Scheme on your computer
Reviewer: ProfessorHarveysNumberOneFan -
- May 5, 2022
Subject: Scheme workflow using Docker Stklos image
course looks very interesting, https://teachyourselfcs.com brought me here

I had the whole issue with trying to figure out how to get the prof's version of Scheme working with all of the function definitions he has, and I wanted to make a simple step-by-step of what my workflow is

I'm assuming you run either Linux or Mac and that you know how to work a command line

1. $ mkdir scheme
2. $ cd scheme && touch simplyscm
3. copy the code from here https://people.eecs.berkeley.edu/~bh/ssch27/appendix-simply.html into the file created in the previous step
4. install docker
5. $ sudo docker pull stklos/stklos:latest
6. $ sudo docker run -v $(pwd):/home -it stklos/stklos:latest
7. stklos> (load "simplyscm")

In case you are wondering how to get out of the container you run:
,quit

Repeat steps 5 to 7 as needed

run
$ docker container prune
once in a while just to get rid of those accumulating stopped containers

# Book Simple Scheme
https://people.eecs.berkeley.edu/~bh/ss-toc2.htm

# Program Structure and Interpretation of Computer Programs
https://romanbird.github.io/sicp/
