
**⚠️ THIS PROJECT IS NOW DEPRECATED ⚠️** 

Following release of [JetBrains Gateway](https://www.gitpod.io/docs/ides-and-editors/jetbrains-gateway) support in Gitpod, JetBrains projector is now no longer officially supported by Gitpod. 

---

# A JetBrains PhpStorm template on Gitpod

This is a [JetBrains PhpStorm](https://www.jetbrains.com/phpstorm/) template configured for ephemeral development environments on [Gitpod](https://www.gitpod.io/).

## Next Steps

Click the button below to start a new development environment:

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/gitpod-io/template-jetbrains-phpstorm)

## Get Started With Your Own Project

### A new project

Click the above "Open in Gitpod" button to start a new workspace. Once you're ready to push your first code changes, Gitpod will guide you to fork this project so you own it.

### An existing project

To get started with JetBrains PhpStorm on Gitpod, add a [`.gitpod.yml`](./.gitpod.yml) file which contains the configuration to improve the developer experience on Gitpod. To learn more, please see the [Getting Started](https://www.gitpod.io/docs/getting-started) documentation.

## Notes & caveats

This template is configured to use JetBrains Projector which is a self-hosted technology that runs IntelliJ-based IDEs and Swing-based apps on servers, allowing you to access them from anywhere using browsers and native apps. 

To learn more about JetBrains Projector head to:

- https://blog.jetbrains.com/blog/2021/03/11/projector-is-out/
- https://jetbrains.github.io/projector-client/mkdocs/latest/

### User Settings

`/workspaces/template-jetbrains-phpstorm` is mounted as the home dir in the Docker container so that settings and projects can be version controlled and thus persisted between launches. After creating the template adjust the bind mount [`.gitpod.yml`](./.gitpod.yml) as required with name of your git repository:


```yml
# Original
sudo docker run --rm -p 8887:8887 -v /workspace/template-jetbrains-phpstorm/.jetbrains:/home/projector-user 

# Updated
sudo docker run --rm -p 8887:8887 -v /workspace/my-jetbrains-repository/.jetbrains:/home/projector-user 
```
