renv
====

script for switching between different R installations on Mac OS X

Every time I download a new version of R, I run its installer. The installer always puts it in

    /Library/Frameworks/R.framework

So after I install each version of R, I rename the R.framework directory to something like
R.framework.bioc214_snowleopard

And then I make a symlink from R.framework.bioc214_snowleopard to R.framework.

The `renv` script in this repository lets me see what the various installed Rs are:

    $ renv 
    302 3.0.2 63987 (none) 2013-09-25 darwin10.8.0
    develMav 3.1.0 65387 (none) 2014-04-10 darwin13.1.0
    develSL 3.1.0 65387 (none) 2014-04-10 darwin10.8.0
    *releaseMav 3.1.0 65387 (none) 2014-04-10 darwin13.1.0
    releaseSL 3.1.0 65387 (none) 2014-04-10 darwin10.8.0

This tells me that the currently active R is nicknamed "releaseMav" (this means there is a link from /Library/Frameworks/R.framework.releaseMav to /Library/Frameworks/R.framework. It shows the versions, svn revisions, dates, and architectures of each version. (darwin10.8.0 is Snow Leopard; darwin13.1.0 is Mavericks).

Note that in my nomenclature devel means BioC devel, not R-devel. 

So if I wanted to switch to the "develSL" version I would do:

sudo renv develSL




> 