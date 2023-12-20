SHARED_SENDER
--------------
#include<sys/ipc.h>
#include<sys/shm.h>
#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<string.h>
int main()
{
void *shared_memory;
char buffer[100];
int shmid;
shmid=shmget((key_t)1222, 1024, 0666|IPC_CREAT);
printf("Key of the Shared Memory is %d\n",shmid);
shared_memory=shmat(shmid,NULL,0);
printf("Process attached at %p\n",shared_memory);
printf("Enter some data to write to shared memory\n");
read(0,buffer,100); 
strcpy(shared_memory,buffer); 
printf("You wrote : %s\n",(char *)shared_memory);
return 0;
}

OUTPUT
-------
Key of the Shared Memory is 31
Process attached at 0x7f316f395000
Enter some data to write to shared Memory
Hello World.This is a Computer program!
You wrote : Hello World.This is a Computer program!



SHARED_RECEIVER
----------------
#include<sys/ipc.h>
#include<sys/shm.h>
#include<stdio.h>
#include<stdlib.h>
#include<unistd.h>
#include<string.h>
int main()
{
void *shared_memory;
char buffer[100];
int shmid;
shmid=shmget((key_t)1222, 1024, 0666);
printf("Key of Shared Memory is %d\n",shmid);
shared_memory=shmat(shmid,NULL,0);
printf("Process attached at %p\n",shared_memory);
printf("Data read from shared memory is : %s\n",(char *)shared_memory);
return 0;
}

OUTPUT
-------
Key of the Shared Memory is 31
Process attached at 0x7f6fa3484000
Data read from shared Memory is : Hello World.This is a Computer program!
