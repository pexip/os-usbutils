# Copyright (C) 2009-2010 Nikolai Kondrashov
#
# This file is part of usbhid-dump.
#
# Usbhid-dump is free software; you can redistribute it and/or modify
# it under the terms of the GNU General Public License as published by
# the Free Software Foundation; either version 2 of the License, or
# (at your option) any later version.
#
# Usbhid-dump is distributed in the hope that it will be useful,
# but WITHOUT ANY WARRANTY; without even the implied warranty of
# MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
# GNU General Public License for more details.
#
# You should have received a copy of the GNU General Public License
# along with usbhid-dump; if not, write to the Free Software
# Foundation, Inc., 51 Franklin St, Fifth Floor, Boston, MA  02110-1301  USA

SUBDIRS = include lib src

dist_noinst_SCRIPTS = bootstrap

ACLOCAL_AMFLAGS = -I m4

dist-hook:
	@set -e; \
	if test -d "$(srcdir)/.git"; then \
		echo Generating ChangeLog; \
		( cd "$(srcdir)" && auxdir/missing --run git log ) > \
			ChangeLog.tmp; \
		mv -f ChangeLog.tmp "$(distdir)/ChangeLog"; \
	else \
		echo Skipping ChangeLog generation: no .git directory >&2; \
	fi

