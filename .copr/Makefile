DNF=/usr/bin/dnf
RPMBUILD=/usr/bin/rpmbuild


srpm:	weston-srpm

rpmbuild:
	$(DNF) -y install rpmbuild

weston-srpm:	rpmbuild
	$(RPMBUILD) -bs \
		--define="_topdir `pwd`" \
		--define="_sourcedir `pwd`" \
		--define="_specdir `pwd`" \
		--define="_srcrpmdir $(outdir)" \
		$(spec)
