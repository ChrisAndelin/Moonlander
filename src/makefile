###############################################################
# Program:
#     Milestone 06, Moon Lander
#     Brother {Burton, Falin, Ercanbrack}, CS165
# Author:
#     your name here
# Summary:
#     Put your summary code here... 
# Above and Beyond
#     When you submit your final project (not for milestones),
#     list anything here that you did to go above and beyond
#     the base requirements for your project.
###############################################################


LFLAGS = -lglut -lGLU -lGL

###############################################################
# Build the main Moon Lander game
###############################################################
a.out: ground.o game.o uiInteract.o uiDraw.o point.o
	g++ ground.o game.o uiInteract.o uiDraw.o point.o $(LFLAGS)
	tar -j -cf moonLander.tar makefile *.h *.cpp

###############################################################
# Individual files
#    uiDraw.o      Draw polygons on the screen and do all OpenGL graphics
#    uiInteract.o  Handles input events
#    point.o       The position on the screen
#    ground.o      Handles the ground / world
#    game.o        Handles the game interaction
###############################################################
uiDraw.o: uiDraw.cpp uiDraw.h
	g++ -c uiDraw.cpp

uiInteract.o: uiInteract.cpp uiInteract.h
	g++ -c uiInteract.cpp

point.o: point.cpp point.h
	g++ -c point.cpp

ground.o: ground.cpp ground.h point.h
	g++ -c ground.cpp

game.o: game.cpp uiDraw.h uiInteract.h point.h ground.h lander.h
	g++ -c game.cpp

lander.o: lander.cpp lander.h 
	g++ -c lander.cpp
#######################################################################
# ADD YOUR ADDITIONAL RULES HERE!
#
# Then, don't forget to add them to the dependecy list for a.out above.
#######################################################################



###############################################################
# General rules
###############################################################
clean:
	rm a.out *.o *.tar
