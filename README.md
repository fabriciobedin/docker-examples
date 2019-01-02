### Add Docker in CMDER
+ 1º Open CMDER
+ 2º Menu -> Settings / Win + Alt + P
+ 3º Add new task in Startup -> Tasks
+ 4º Past the directory of the docker in task parameters
`/dir "C:\Program Files\Docker Toolbox"`
+ 5º Past the arguments of the docker in Commands - Params
`"C:\Program Files\Git\bin\bash.exe" --login -i -new_console:C:"C:\Program Files\Docker Toolbox\docker-quickstart-terminal.ico" "C:\Program Files\Docker Toolbox\start.sh"`
+ 6º Save and enjoy :)

### Commands
+ `docker run -ti --rm ubuntu bash`
  - `-ti` -> Iterative mode, it leaves you know about what is happening while docker is running.
