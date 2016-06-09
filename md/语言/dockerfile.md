---
Order: 11
Area: languages
TOCTitle: Dockerfile
ContentId: 42F8B9F8-BD03-4159-9479-17C5BDE30531
PageTitle: Working with Dockerfiles in Visual Studio Code
DateApproved: 4/14/2016
MetaDescription: Find out how to get the best out of Visual Studio Code and Docker.
---

# Working with Docker

[Docker](http://www.docker.com) is a very popular container platform that lets you easily package, deploy, and consume applications and services. Whether you are a seasoned Docker developer or just getting started, Visual Studio Code makes it easy to author `Dockerfile` and `docker-compose.yml` files in your workspace.

## Install the Docker extension

Docker support for VS Code is provided by an extension.  To install the Docker extension, Press `kb(workbench.action.showCommands)`, type "ext install" and run the **Extensions: Install Extension** command to bring up the Marketplace extension list. Now type "docker" to filter the results and select the [Dockerfile and Docker Compose File (yml) Support](https://marketplace.visualstudio.com/items?itemName=PeterJausovec.vscode-docker) extension.

![Select Docker extension](images/docker/installdockerextension.png)

## Dockerfiles

With Docker, you can build images by specifying the step by step commands needed to build the image in a `Dockerfile`. A Dockerfile is simply a text file that contains the build instructions.

VS Code understands the structure of Dockerfiles as well as the available set of instructions, meaning we can give you a great experience when authoring these files in the tool.

1. Create a new file in your workspace named `Dockerfile`
2. Press `kb(editor.action.triggerSuggest)` to bring up a list of snippets corresponding to valid `Dockerfile` commands

 ![Dockerfile snippets](images/docker/dockerfileintellisense.png)

3. Press `kbstyle(Tab)` to move between fields within the snippet. For example, with the `COPY` snippet you can fill in the `source` and then press `kbstyle(Tab)` to move to the `dest` field.

 ![Dockerfile snippet navigation](images/docker/dockerfiletemplate.png)

In addition to snippets for authoring your `Dockerfile`, Visual Studio Code will provide you with a description of any Docker command you hover over with the mouse. For example, when hovering over `WORKDIR` you will see the following.

![Dockerfile hover tooltip](images/docker/dockerfiletooltip.png)

For more information on Dockerfiles, check out [Dockerfile best practices](
https://docs.docker.com/articles/dockerfile_best-practices/) on [docker.com](http://docker.com).

## Docker Compose

[Docker Compose](https://docs.docker.com/compose/) lets you define and run multi-container applications with Docker. You define what the shape of these containers look like with a file called `docker-compose.yml`.

Visual Studio Code's experience for authoring `docker-compose.yml` is also very rich, providing IntelliSense for valid Docker compose directives and it will query Docker Hub for metadata on public Docker images.

1. Create a new file in your workspace called `docker-compose.yml`
2. Define a new service called `web:`
3. On the second line, bring up IntelliSense by pressing `kb(editor.action.triggerSuggest)` to see a list of all valid compose directives.

 ![Docker Compose IntelliSense](images/docker/dockercomposeintellisense.png)

4. For the `image` directive, you can press `kb(editor.action.triggerSuggest)` again and VS Code will query the Docker Hub index for public images.

 ![Docker Compose image suggestions](images/docker/dockercomposeimageintellisense.png)

VS Code will first show a list of popular images along with metadata such as the number of stars and description. If you continue typing VS Code will query the Docker Hub index for matching images, including searching public profiles. For example, searching for `Microsoft` will show you all the public Microsoft images.

 ![Docker Compose Microsoft image suggestions](images/docker/dockercomposesearch.png)
