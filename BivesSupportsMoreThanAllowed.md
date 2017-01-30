Bives Supports a wider Language 
================================
Since the capabilities of provided parsers for the markup languages used to encode computational models are not sufficient for the use in /BiVeS it provides own parsers to read e.g. CellML or SBML models. (see e.g. http://sems.uni-rostock.de/trac/bives-cellml/wiki//CellMlReading and http://sems.uni-rostock.de/trac/bives-sbml/wiki//SbmlReading). These parsers allow for a mixture of versions of the specification of the corresponding markup languages. For example, in /BiVeS a model encoded in 
* [http://www.cellml.org/specifications/cellml_1.0 CellML version 1.0] may import other CellML documents, even if that feature was not introduced before [http://www.cellml.org/specifications/cellml_1.1 CellML 1.1]. It is the same for SBML models.
* [SBML Level 3](http://sbml.org///Documents/Specifications#SB/M/L_Level_3) is allowed to use Species types, even if the SBML specification doesn't support Species types after [Level 2](http://sbml.org///Documents/Specifications#SB/M/L_Level_2).

However, all models valid according to the original specification should be valid in /BiVeS.
If you just want to read models and do not care much about the underlying markup language you are free to use /BiVeS in your projects.