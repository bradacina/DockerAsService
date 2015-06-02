# DockerAsService on Windows

1. Create a local user with admin privileges
2. Install Boot2Docker for this user
3. Setup Virtual Box port forwarding for SSH and whatever other forwarding you need
4. Use Boot2Docker to start the boot2docker-vm which will generate the ssh keys in your %HOME%/.ssh folder
5. Copy the ssh keys to whichever machine you will be using to ssh into the docker vm
6. Optionally use PuttyGen to generate a PPK file from the ssh key

7. Shut down the docker vm
8. Exit Virtual Box if you have it open
9. Clone this Repo
10. Build
11. Move the resulting executable and DockerAsService.json file to a folder of your choosing
12. Open a cmd prompt and navigate to the folder you chose in step 11
13. Execute DockerAsService.exe -service install
14. Open services.msc and find the Docker As Service service
15. Right click the service and go to Properties > Logon tab
16. Enter the username/pass for the local admin user that you created in step 1
17. Hit Apply
18. Start the service
19. Use the ssh key from step 5 or ppk file from step 6 to login into the docker vm

