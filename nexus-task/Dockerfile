FROM sonatype/nexus3:3.45.1
#Use of versioning is to avoid latest issues that can occur if the latest image does not support something that we desire
# example we had 3.45.1 => which supports the 0.45 nexus blob plugin that we install in the steps below

# This is not the best way to save the credentials ( we can create a docker secret then import it here )
ENV GOOGLE_APPLICATION_CREDENTIALS=key.json


#Adding the blob.kar package inside of our docker build in order to load it when it starts
# Downside is we need either to save this image somewhere or use volumes if we want to mount this to a clean nexus instance
ADD nexus-blob.kar /opt/sonatype/nexus/deploy
