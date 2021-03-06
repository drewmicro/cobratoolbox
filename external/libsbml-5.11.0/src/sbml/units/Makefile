## src/sbml/units/Makefile.  Generated from Makefile.in by configure.
##
## Filename    : Makefile.in
## Description : Makefile template for libsbml main sources
## Author(s)   : SBML Team <sbml-team@caltech.edu>
## Organization: California Institute of Technology
## Created     : 2004-06-11
## 
## <!--------------------------------------------------------------------------
## This file is part of libSBML.  Please visit http://sbml.org for more
## information about SBML, and the latest version of libSBML.
##
## Copyright (C) 2013-2014 jointly by the following organizations:
##     1. California Institute of Technology, Pasadena, CA, USA
##     2. EMBL European Bioinformatics Institute (EMBL-EBI), Hinxton, UK
##     3. University of Heidelberg, Heidelberg, Germany
##
## Copyright (C) 2009-2013 jointly by the following organizations: 
##     1. California Institute of Technology, Pasadena, CA, USA
##     2. EMBL European Bioinformatics Institute (EMBL-EBI), Hinxton, UK
##  
## Copyright (C) 2006-2008 by the California Institute of Technology,
##     Pasadena, CA, USA 
##  
## Copyright (C) 2002-2005 jointly by the following organizations: 
##     1. California Institute of Technology, Pasadena, CA, USA
##     2. Japan Science and Technology Agency, Japan
## 
## This library is free software; you can redistribute it and/or modify it
## under the terms of the GNU Lesser General Public License as published by
## the Free Software Foundation.  A copy of the license agreement is provided
## in the file named "LICENSE.txt" included with this software distribution
## and also available online as http://sbml.org/software/libsbml/license.html
## ------------------------------------------------------------------------ -->


# -----------------------------------------------------------------------------
# Configuration variables
# -----------------------------------------------------------------------------
# Some of the following are substituted automatically by `configure'.  If
# you are looking at "Makefile", do not edit these values; instead, run the
# configure script at the top level of the src tree.  It will recreate
# "Makefile".

include ../../../config/makefile-common-vars.mk

# `srcdir' points to the current directory, but should be set by configure.
# `subdir' must be set manually to the relative dir under `srcdir'.  Don't 
# set `subdir' to an absolute path, or some `make' actions will fail.

srcdir  = .
thisdir = src/sbml/units

# Variables `headers', `sources', `libraries', `extra_CPPFLAGS',
# `extra_CXXFLAGS', `extra_LDFLAGS' and `distfiles' are used by the default
# rules in `makefile-common-actions.mk' included at the end.

headers =                    \
  UnitFormulaFormatter.h     \
  FormulaUnitsData.h         \
  UnitKindList.h

header_inst_prefix = units

sources =                    \
  UnitFormulaFormatter.cpp   \
  FormulaUnitsData.cpp       \
  UnitKindList.cpp

# Variables `subdirs', `headers', `sources', `libraries', `extra_CPPFLAGS',
# `extra_CXXFLAGS', `extra_LDFLAGS' and `distfiles' are used by the default
# rules in `makefile-common-actions.mk' included at the end.

ifdef USE_EXPAT
  extra_CPPFLAGS += $(EXPAT_CPPFLAGS)
  extra_LDFLAGS  += $(EXPAT_LDFLAGS)
  extra_LIBS     += $(EXPAT_LIBS)
endif

ifdef USE_XERCES
  extra_CPPFLAGS += $(XERCES_CPPFLAGS)
  extra_LDFLAGS  += $(XERCES_LDFLAGS)
  extra_LIBS     += $(XERCES_LIBS)
endif

ifdef USE_LIBXML
  extra_CPPFLAGS += $(LIBXML_CPPFLAGS)
  extra_LDFLAGS  += $(LIBXML_LDFLAGS)
  extra_LIBS     += $(LIBXML_LIBS)
endif

subdirs = test

# `distfiles' determines the files and directories included in a distribution.
# `distfiles_exclude' is used to filter out specific items, so that even if
# they appear in `distfiles', they will not be copied in the distribution.

distfiles = $(sources) $(headers) Makefile.in


# -----------------------------------------------------------------------------
# Primary build actions
# -----------------------------------------------------------------------------

# The default action is to remake everything.  Those rules which are not
# defined below are defined in makefile-common-actions.mk.

all: Makefile default


# -----------------------------------------------------------------------------
# Checking.
# -----------------------------------------------------------------------------

check: check-recursive


# -----------------------------------------------------------------------------
# Tags.
# -----------------------------------------------------------------------------

tags: etags ctags


# -----------------------------------------------------------------------------
# Installation
# -----------------------------------------------------------------------------

# This doesn't actually get installed as a library.  The main libsbml library
# (in ../sbml) slurps in the object files when it's built.  Here we just put
# in 'all' as a default to make sure files get compiled if someone does
# 'make install' from the top level without first doing a 'make'.

install: all install-headers

installcheck: all installcheck-headers

uninstall: uninstall-headers


# -----------------------------------------------------------------------------
# Cleaning.
# -----------------------------------------------------------------------------

clean: clean-normal clean-recursive

distclean: distclean-normal distclean-recursive

mostlyclean: mostlyclean-normal mostlyclean-recursive

maintainer-clean: maintainer-clean-normal maintainer-clean-recursive


# -----------------------------------------------------------------------------
# Creating distribution (for libSBML maintainers only)
# -----------------------------------------------------------------------------

dist: all dist-normal dist-recursive

distcheck: all distcheck-normal distcheck-recursive


# -----------------------------------------------------------------------------
# Miscellaneous
# -----------------------------------------------------------------------------

include ../../../config/makefile-common-actions.mk


# -----------------------------------------------------------------------------
# End.
# -----------------------------------------------------------------------------

