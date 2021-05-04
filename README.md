# make-glossary
Simple bash script to generate LaTeX glossary files from .csv files

LaTeX offers cool capabilities, one of them being the glosssary package through which one can:
*  Generate lists of glossaries and acronyms.
*  display the full expansion of an acronym (or an abbreviation) on the first call, after which it will be displayed as the abbreviation.

The problem is that one must define these glossary items and acronyms in a format which takes up time to code.
Fortunately for us, the format is generatable by code!

My scripts will help you convert the .csv lists (acronym.csv and glossaries.csv) into a LaTeX glossary file.
Furthermore, using cron jobs, one can automatically compile a glossary file, all one has to do is update the .csv files with whatever info they need.

Usage:
* Copy this repo to your folder with your .tex file
* Make sure you have the 'glossaries' package installed: https://ctan.org/pkg/glossaries?lang=en
* Include glossary.tex in your .tex file as shown in the example with command `\includeglossary{glossary}`
* Change path to your LaTeX directory in makeglossary.sh
* Change execution permissions for makeglossary.sh using `chmod 700 makeglossary.sh`
* Execute makeglossary.sh, by running in this in the parent directory `./makeglossary.sh`

Cron jobs on Linux (Ubuntu):
- Put following commands in crontabs editing cron jobs with this command: `crontabs -e`
- Run scheduled execution every 2 minutes: `*/2 * * * * /path/to/directory/makeglossary.sh`
