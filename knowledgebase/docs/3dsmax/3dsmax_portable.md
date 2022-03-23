# Making 3ds Max portable

## Introduction

With the release of 3ds Max 2022.3 Autodesk ships **_Robust Pipeline Integration_**.
This mostly introduces the posibility to configure many of 3ds Max's paths through
environment variables. This offers a lot of possibilities. This enables a lot of
things impossible before, like loading plugins from arbitrary locations without
plugin.ini by simply adding paths to an environment variable.

Amongst the usual suspects there is also one very special easy to overlook new
environment variable: `ADSK_3DSMAX_x64_<year>`. This enables setting the root 
folder of 3ds Max and running it from arbitrary places. 

### Pre-Requisites on target machines

#### Installing the licensing service and the SSO component

Here is the first paragraph

```Some multi line code block```

#### Registering with the licensing service

### Setting up a portable environment for Max

### Bonus: Building a rez package

### Appendix: List of environment variables supported as of 2022.3

| Name                                     | Description                                                                                                                                                                                                                                                                   |
| ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| ADSK\_3DSMAX\_x64\_ <year>               | The path to the 3ds Max install. Created by the installation process. On systems where 3ds Max was copied instead of installed, this variable needs to be defined manually.                                                                                                   |
| ADSK\_3DSMAX\_ APPDATA\_DIR              | The path used by 3ds Max to read and write local user data. By default this location is C:\\Users\\<username>\\AppData\\Local\\Autodesk\\3dsMax\\<year> - 64bit\\<lang>                                                                                                       |
| ADSK\_3DSMAX\_SCRIPTS\_ADDON\_DIR        | A list of semicolon-delimited paths, used in addition to the **Additional Scripts** folder defined in the Configure User and System Paths dialog.                                                                                                                             |
| ADSK\_3DSMAX\_STARTUPSCRIPTS\_ADDON\_DIR | A list of semicolon-delimited paths, used in addition to the **Additional Startup Scripts** folder defined in the Configure User and System Paths dialog.                                                                                                                     |
| ADSK\_3DSMAX\_MACROS\_ADDON\_DIR         | A list of semicolon-delimited paths, used in addition to the **Additional Macros** folder defined in the Configure User and System Paths dialog.                                                                                                                              |
| ADSK\_3DSMAX\_ICONS\_ADDON\_DIR          | A list of semicolon-delimited paths, used in addition to the **Additional Icons** folder defined in the Configure User and System Paths dialog.                                                                                                                               |
| ADSK\_3DSMAX\_PLUGINS\_ADDON\_DIR        | A list of semicolon-delimited paths, used in addition to the **Additional MAX plug-ins** folder defined in the Configure User and System Paths dialog.                                                                                                                        |
| ADSK\_3DSMAX\_ASSETS\_XREFS\_DIR         | A list of semicolon-delimited paths, used in addition to the Xrefs paths defined in the Configure Project Paths dialog.                                                                                                                                                       |
| ADSK\_3DSMAX\_ASSETS\_MAPS\_DIR          | A list of semicolon-delimited paths, used in addition to the External Files paths defined in the Configure Project Paths dialog.                                                                                                                                              |
| ADSK\_3DSMAX\_PROJECT\_FOLDER\_DIR       | The path for the location for project data (such as material libraries, render presets, render output, etc). If this variable is defined but the specified folder does not exist, 3ds Max creates it. This envar takes precedence over the ProjectFolder value in 3dsmax.ini. |
| ADSK\_3DSMAX\_USERSETTINGS\_DIR          | The path for reading and writing user settings. If this variable is defined but the specified folder does not exist, 3ds Max creates it.                                                                                                                                      |
| ADSK\_3DSMAX\_SDK\_<YEAR>                | The fully-qualified path for the 3ds Max SDK, if installed.                                                                                                                                                                                                                   |
| ADSK\_3DSMAX\_SESSION\_LOG               | The path to the 3ds Max session log.                                                                                                                                                                                                                                          |
| ADSK\_APPLICATION\_PLUGINS               | A list of semicolon-delimited paths, specifying root folders from which to load additional 3rd party application plug-ins. Each folder can either contain a plug-in, or a collection of folders containing plug-ins.                                                          |