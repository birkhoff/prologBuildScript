prologBuildScript
=================

The prologBuildScript provides a simple way to use sicstus splfr linker

In the curreng state your prolog files must be located in the folder you defined in the dynamic property <b>pl_srcs</b>
and you c/cpp files must be located in the folder you defined for the property <b>c_srcs</b>

By default these folder are defined as:   
\tproject.ext.c_srcs = "${projectDir}/src/cpp/"
\tproject.ext.pl_srcs = "${projectDir}/src/prolog/"

Caution!
Please be aware that you can only link one prolog file to multiple c files.
All other files in pl_srcs should be test files.

By default the script will look for one prolog file that is located in pl_srcs that doesn't include the word "test" in 
its name.
But you can also define the file for the linker by yourself via project.ext.pl_file = "name_of_prolog_file.pl"

If you have test files you can include them with project.ext.pl_test_file = "your_test_file.pl"
By default the script will take your linked prolog file as test file.

Your tests predicates can be defined as project.ext.pl_tests = "test_1,test_2,halt."
By default it will use project.ext.pl_tests = "test,halt."


currently under development

© 2013 Mike Birkhoff
