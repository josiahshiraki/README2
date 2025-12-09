# README #1

## Author: Josiah Shiraki
## Purpose: Documenting the starter labs (Lab 06–11)

# Lab06: Display
This lab focused on getting an image on a display
## Challenges
### Getting Used to the display syntax
There where a lot of new functions that were specific to writing to the display that were hard to get to know, but once understood it was fun to draw whatever I could think of.

# Lab07: File 
This lab's purpose was to get to know how to use files within folders in the starter doorbell repo.
## Challenges
### Finding the correct file path
The file path is really important to get right, if it's in a specific format or the .extension is wrong, it will break the program.

# Lab08: Camera
The object of this lab was to learn how to take a picture and handle the raw data in a buffer and writing it to a .bmp file.
## Challenges
### Hardware issues
The software wasn't too bad, but my hardware was not working, the bulk of this lab was reconfiguring the hardware so the camera worked.
### Malloc
Another interesting but new concept to me, knowing how to use it and what to pass in and what it returns.

# Lab09: Client
purpose of this was to learn how to use the connection of the rasberry pi of the internet sending data from it to a web server.
## Challenges
### Snytax(like always)
The syntax for this lab was very foreign to me as it was the first time I've done with web sockets and sending information from hardware to software via internet. This lab required a lot of research outside the lab to get the functions to work properly. 

# Lab10: Threaded Client
Use a thread to "multitask" on the rasberry pi, i.e. displaying the menu while also sending the image to the web server.
## Challenges
### Learning what a thread actually is
I had to do some background reseach and even watch a explanatory video to understand what a thread is in code so that I could implement it easier. 
## Code for a basic thread
```C
#include <unistd.h>   // Library that includes sleep()
#include <pthread.h>  // Library that includes pthreading types and functions

void *print_msg(void *unused)
{
    while(1)
    {
        printf("I'm in a thread!\n");
        sleep(2);     // Sleeps for 2 seconds
    }

    return NULL;
}

int main()
{
    pthread_t my_thread;
    pthread_create(&my_thread, NULL, print_msg, NULL);

    while(1)
    {
        printf("I'm in main!\n");
        sleep(1);
    }

    return 0;
}
```

## Lab11: Doorbell
This was the final lab for the doorbell, we learned how to use a daemon to run the doorbell independent from VS code
## Challenges
### Getting the lab specs correct
Setting up the Daemon wasn't hard, but I didn't read the lab specs for the final passoff carefully so I had to keep on redoing and rediting code so that its finally was up to the specifications.


