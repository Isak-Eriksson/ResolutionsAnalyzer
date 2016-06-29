# ResolutionsAnalyzer

Resolutions Analyzer is a tool for analyzing merge-conflicts resolutions. The tool was used in a study where the 20 top starred GitHub projects were analyzed. The result data is available in Results.xlsx.

##Install and run:
Resolutions Analyzer analyzes the output of Conflicts Analyzer. Thus, it is required that Conflicts Analyzer is run on projects of the user's choice first (see https://github.com/patwal/conflictsAnalyzer for instructions).

###Running the .jar

Resolutions Analyzer takes as argument the path to the conflict reports root folder of the projects analyzed, produced by Conflicts Analyzer. It also takes as argument the path to the repository download folder (the same as in the configuration for Conflicts Analyzer, *downloads.path*). Download and extract ResolutionsAnalyzer.zip from the repository, then run:

`java -jar ResolutionsAnalyzer.jar </path/to/conflictreports/> </download.path/>`

It is important that ResolutionsAnalyzer.jar is executed in the same folder as scripts/ (packaged next to ResolutionsAnalyzer.jar in the .zip file).

###Running it in Eclipse
Running Resolutions Analyzer from Eclipse can be done by cloning the repository and creating a new Java project in Eclipse. 

`git clone https://github.com/Isak-Eriksson/ResolutionsAnalyzer`

Then you can either import the source files from the src/ folder and the scripts from the scripts/ folder into your newly created project, or you can create symbolic links of the src/ and scripts/ folders into your project folder.

Resolutions Analyzer uses the JXL library. Add it to the Java build path by importing jxl.jar from the repository.

Click Run -> Run configurations… then browse to your Resolutions Analyzer project. Click the tab Arguments and input </path/to/conflictreports/> </download.path/> as Program arguments.

Running the project will create Results.xls in the project path.

