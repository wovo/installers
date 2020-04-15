To start with bmptk/hwib on Ubuntu under VMware:

- get WMware workstation player (or VirtualBox, or run plain Linux)
- get the Ubuntu 18.04.2 LTS ISO from https://www.ubuntu.com/download/desktop
- create an image from the iso (remember the password!) - this will take some time...
- log in, open a terminal, click through the friendly welcome screens
- run these commands in your home directory:
   - sudo apt-get install -y git
   - git clone https://www.github.com/wovo/installers
   - chmod 777 ~/installers/ubuntu; ~/installers/ubuntu
   
- for convenience: set the Firefox start pagina to the hwlib documentation
   - cd ~/hwlib
   - firefox index.html &
   - settings->prefrences->home->homepage:custom urls->use current page   
   
- to verify the various types of builds, run the indicated commands
   - basic native:
      - cd ~/v1oopc-examples/*-hello; make run
      (after building the executable should run and print "Hello world")
   - native with graphics:
      - cd ~/v1oopc-examples/*-rectangle; make run
      (running should show a window with a rectangle)
   - basic Arduino Due:
      (VMware must have the focus while you plug in the Arduino)
      - cd ~/v1oopc-examples/*-blink-hwlib; make run
      (after building the executable should download to the Due and the LED should blink)
   - Arduino Due serial link:
      (assuming you have the Arduino Due still plugged in)
      - cd ~/v1oopc-examples/*-cout; make run 
      (You should see "cout demo" and a few more lines)
	  
- to start with codelite:
<<<<<<< HEAD
   - cd ~/v1oopc-examples; ./update*.bat; codelite __codelite.workspace &
   (click next on a few screens)
   - double-click on the first project (it must be black); select build->run
   (a few more screens; select 'only run'; select any compiler (g++ is OK))
=======
   - cd ~/v1oopc-examples; ./update*.bat; sudo codelite __codelite.workspace &
   (click next on a few screens; I prefer the "Classic Eclipse" color scheme)
   double-click on the first project (it must be black); select build->run
   (a few more screens; select 'Execute' and check the box; wen asked, select any compiler (g++ is OK))
>>>>>>> 3b99d06f3a39ec399414a1f7d1225e5a7d91c336
   (the screen with the result can end up behind the CodeLite screen)
   



   