# Makefile.am
#     	Copyright (C) 2002 Free Software Foundation, Inc.
#
# This file is part of GnuPG.
#
# GnuPG is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 3 of the License, or
# (at your option) any later version.
#
# GnuPG is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with this program; if not, see <https://www.gnu.org/licenses/>.

## Process this file with automake to produce Makefile.in

if TEST_LIBTSS
tpm2dtests = tpm2dtests
else
tpm2dtests =
endif

SUBDIRS = gpgscm openpgp cms migrations gpgme pkits $(tpm2dtests) .

GPGSM = ../sm/gpgsm


EXTRA_DIST = run-tests.scm gpgconf.ctl.in      \
             fake-pinentries/README.txt        \
             fake-pinentries/fake-pinentry.php \
             fake-pinentries/fake-pinentry.pl  \
             fake-pinentries/fake-pinentry.py  \
             fake-pinentries/fake-pinentry.sh  \
	     ChangeLog-2011

CLEANFILES =  x y z out err

if !HAVE_W32_SYSTEM
noinst_PROGRAMS = asschk
endif

asschk_SOURCES = asschk.c
