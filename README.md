# sapthesisdown

This project is an adaptation of the [thesisdown](https://github.com/ismayc/thesisdown) package to the LaTeX template [sapthesis](http://biccari.altervista.org/c/informatica/latex/sapthesis.php).

Currently, the PDF and gitbook versions are fully-functional.  The word and epub versions are developmental, have no templates behind them, and are essentially calls to the appropriate functions in bookdown.

Arguments to be passed in the YAML header are the following (**`bold`** indicates those which are mandatory, while `regular` denotes that the field is optional):

### General Options

* **`degree`** : possible choices are
    + `PhD` - Option to typeset a *Dottorato di Ricerca* (PhD) thesis.
    + `LaM` - Option to typeset a *Laurea Magistrale* (Master's degree) thesis.
    + `Lau` - (default) Option to typeset a *Laurea* (Bachelor's degree) thesis.
    + `MasterP` - Option to typeset a thesis for a *Master di primo livello* (First level master).
    + `MasterS` - Option to typeset a thesis for a *Master di secondo livello* (Second level master).
    + `TFA` - Option to typeset the final report for a *Tirocinio Formativo Attivo*.
    + `Specialization` - Option to typeset a thesis for a *Specializzazione*.

* `options`:
    + `draft` - the usual `draft` option of the LaTeX Standard Classes.
    + `oneside` - the usual `oneside` option of the LaTeX Standard Classes.
    + `twoside` - (default) the usual `twoside` option of the LaTeX Standard Classes .
    + `bn` - this option typesets the title page in black and white (using the b/w logo, `sapienza-MLblack-pos.pdf`, instead of the colored one) and passes the `monochrome` option to `color` and 
`xcolor` packages.
    + `noexaminfo`- suppress all the final exam informations. Indeed, by default,`sapthesis` shows some information about the final thesis discussion on the back of the title page. When `noexaminfo` is given as option, it shows the phrase ``Thesis not yet defended''. Otherwise, as explained later, giving the commands 
`examdate` and `examiner`the date and
the examiners list are shown.
    + `italian` or `english` (default) - explicitly declare the language of 
the title page. Useful when you want to write the title page in a language 
and the thesis in a different language.
    + `nodefaultfont` - avoid the loading of packages `fontenc`, `textcomp` and `lmodern`.
    + `fem` - use the feminine (only Italian): shows "candidata" instead of "candidato".


### Title Options

* **`title`**: Title of the Thesis

* `subtitle`: Subtitle (try to avoid a subtitle).

* **`author`**: Author (student's name).

* **`IDnumber`**: ID number (*matricola* in Italian).

* **`course`**: Use the official Italian name of the course.

* **`courseorganizer`**: Course organizer.

* **`submitdate`**: Use the form "April 2009" for PhD's and the form "2009/2010" for Laurea theses.

* `AcademicYear`: Alias for \texttt{\bs submitdate}. Academic Year.

* **`copyyear`**: Copyright year (usually the  graduation year). 

* **`advisor`**: You must specify at least one advisor.
If you have more than one advisor, put several advisor commands in the correct order:\\
\texttt{\bs advisor\{Prof.~Pippo\}} \texttt{\bs advisor\{Dr.~Pluto\}}

*[\texttt{\bs coadvisor[\dots]\{\dots\}}] Optional. Co-advisors of the thesis. 
Same syntax of the \texttt{\bs advisor} command. If the optional argument \texttt{ext} is specified, ``External advisor'' will be printed instead of ``Co-Advisor''.

* `reviewer`: Reviewers of the thesis. 
Same syntax of the \texttt{\bs advisor} command. The list of the reviewer is preceded by the a text which can be specified by the \texttt{\bs reviewerlabel\{\dots\}} command.

* **`authoremail`**: Email of the thesis author.It is automatically hyper-linked if \textsf{hyperref} package is loaded.

* `versiondate`: Date version of the thesis.

* `website`: Thesis website. Automatically 
hyper-linked if \textsf{hyperref} package is loaded.

* `ISBN`: ISBN

* `copyrightstatement`: Specify a copyright statement that will be printed in place of the default one.

* `examdate`: Date of the final exam.

* `examiner`: Specifies the members of the
board of examiners of the final exam. Usage similar to \texttt{\bs advisor} command. 

* `cycle`: Mandatory only for PhD's. 

* `director`: Mandatory only for Specialization.

* `tutor` and `tutorcoord`: Mandatory only for TFA.

* `schoolname`: Mandatory only for TFA, name of the school.

* `schooladdress`: Mandatory only for TFA, school's address.

* `schoolwebsite`: Mandatory only for TFA, school's website.

* `schoolprincipal`: Mandatory only for TFA, school's principal.

