Readme.txt
----------

This folder provides an evaluation version of Trinity and a collection of 
datasets on which it can be evaluated.

To run it, execute the following command:

	java -jar Trinity-1.0.jar Tokeniser.cfg dataset-folder min max

For instance, try the following:

	java -jar Trinity-1.0.jar Tokeniser.cfg datasets/Books/www.abebooks.com 1 75

This will analise the pages in this dataset and will create output something 
like this:

	www.abebooks.com 0.096875
	
This indicates that the dataset was processed and that it took 0.096875 CPU seconds
to learn a regular expression that represents the template from which these pages 
were generated.  The rest of the time is used to tokenise the input documents, for 
which we rely on GNU Regex 1.1.4. 

The rule learnt is stored in a file called rules.regex that is stored in the same 
folder as the dataset.  It is a regular expression that can be executed on any modern
regex engine.  We tested it with GNU Regex 1.1.4 and .NET 4.0 Regex Engine.


