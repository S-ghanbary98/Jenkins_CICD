# Jenkins

## Building a New Project

Simple steps need to be taken to build a new project. 

- Firstly select `new Item`, enter the name of a project, in this case `eng89 Shervin`. This is a `freestyle project`.
- Enter a Description. E.g 'jenkins server for project'.
- Ensure to select the checkbox labelled `Discard old build` and to enter 3 in `	Max # of builds to keep`.
- Scroll to bottom of page and select dropdown menu labelled `Add build step`, select `Execute shell`.
- Enter code to be run initially when build is run. This can be seen below. Then apply and save.
##### Execute Shell
```python
uname -a
pwd
```
- Hover over project and select `build now`, then select `console output` in history. 
- If successful the following message will be seen in the last line. `Finished: SUCCESS`.

## Triggering Separate Project
- Follow steps above and create a new project with a different name. e.g `eng89 shervin pipeline`.
- Select `configure` on first build.
- scroll to `Post-Build Actions` and select `Build other projects`.
- Now run first project and if successful the following message will be seen in the console output.
```python
Triggering a new build of eng89 Shervin pipeline
Finished: SUCCESS
```


