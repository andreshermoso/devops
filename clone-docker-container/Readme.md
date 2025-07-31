## Docker container from EC2 

1. Container to clone ( docker ps command )

2. Export container as a TAR archive, this will create a snapshot of the container filesystem ( docker export command )
  
3. Import the TAR archive. Once the TAR archive is on your local machine, you can import it using the ( docker import command ). This will create a Docker image from the TAR archive.

4. Run the container locally ( docker run command )

5. [clone-docker](clone-docker)
