### General Information

Viper Module Template for [Generamba](https://github.com/rambler-digital-solutions/Generamba) code generator inspired on [Ramber Viper Controller templates](https://github.com/rambler-digital-solutions/generamba-catalog).

OnSight team use this viper template for generating modules on Viper architecture with UIViewController playing as a View.

----
### Generating Rambafile

- Open **Terminal** app inside `pod` project folder:
    - `generamba setup`

**The list of questions for installation**

- The company name which will be used in the headers:
    - `Client company name`

- The name of your project is TestGeneramba. Do you want to use it? (yes/no)
    - `yes`

- The project prefix (if any):
    - leave this answer is empty, just press `Enter`

- The path to a .xcodeproj file of the project is 'TestGeneramba.xcodeproj'. Do you want to use it? (yes/no)
    - `..\prj\TestGeneramba.xcodeproj` - where **TestGeneramba** it's project name

- Select the appropriate target for adding your MODULES (type the index):
    - leave this answer is empty, just press `Enter`

- Are you using unit-tests in this project? (yes/no)
    - `yes` - only in case if this project will contain tests, in other cases `no`

- Do you want to add all your modules by one path? (yes/no)
    - `yes`

- Are you using Cocoapods? (yes/no)
    - `yes`

- The path to a Podfile:
    - `Podfile` - because in our project structure, Rambafile will placed near with Podfile

- Are you using Carthage? (yes/no)
    - `no`

- Do you want to add some well known templates to the Rambafile? (yes/no)
    - `yes` - just for case, when we want to try generate modules with standart templates, if not then choose option `no`


### Creating Templates


- Open file **`Rambafile`** generated file after setup Generamba for project

- Add template to the **`templates`** list at the bottom of the document:
       - `- {name: osvip_module, git: 'https://bitbucket.org/onsightukraine/osvip_module'}`

- Run command:
       - `generamba template install`

- Check if new template was added to the list:
       - `generamba template list`

- Generate new module with new template:
      - `generamba gen RegisterModule osvip_module` - where **RegisterModule** it's new module name
