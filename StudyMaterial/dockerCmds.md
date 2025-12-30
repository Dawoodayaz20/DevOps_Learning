# Docker syntax

1. FROM image[:tag] [AS name]
  - *FROM* command specifies the base image to use for the new image.
    * e.g: FROM ubuntu:20.04

2. WORKDIR /path/to/workdir
  - *WORKDIR* command specifies the working directory.
    * e.g: WORKDIR /app

3. COPY [--chown=<user>:group>] <src>... <dest>
  - *COPY* command lets you copy the files from directories or the build context to the image.
    It means bringing your choice of cooking tools and ingerdients to your cooking spot.
    * e.g: COPY . /app

4. RUN <command>
  - *RUN* will run the command you want in the powershell. 
    * e.g: RUN npm run dev

5. EXPOSE <port> [<port>/<protocol>]
  - *RUN* tells docker that the program will be listening to the specified network port at runtime.
    * e.g: EXPOSE 3000

6. ENV KEY=VALUE
  - *ENV* sets environment variables during the build process.
    * e.g: ENV NODE_ENV=production

7. ARG <name>[=<default value>]
  - *ARG* is for defining built time variables.
  * e.g: ARG NODE_VERSION=20

8. VOLUME ["/data"]
  - *VOLUME* is for creating a mount point for externally mounted volumes. It tells that where you can mount or connect the external storage with the container. 
    * e.g: VOLUME /myvol 

9. CMD ["executable","param1","param2"]
  - *CMD* provides the default commands to run when the container starts.
    * e.g: CMD["param1","param2"]
      CMD["npm","run","dev"]
      CMD npm run dev

10. CMD ["executable","param1","param2"]
  - *ENTRYPOINT* specifies the default execuatble too be run when the container starts. 
    * CMD command param1 param2 e.g: CMD npm run dev
    1. It's like having a default dish for everey customer until someone specifically orders something else.
    2. *ENTRYPOINT* != *CMD*.
      ~ Because CMD is flexible and can be overriden while ENTRYPOINT cannot be changed. 
      ~ CMD : Default executable.(It can be changed)
      ~ ENTRYPOINT Fixed startng point (from where the container will start)
    3. If both have to be used, CMD's arguments will be passed to the ENTRYPOINT's arguments.