# Contributor: Anonymous
# Generator  : CPANPLUS::Dist::Arch 1.29

pkgname='perl-devel-checklib'
pkgver='1.01'
pkgrel='1'
pkgdesc="check that a library is available"
arch=('any')
license=('PerlArtistic' 'GPL')
options=('!emptydirs')
depends=('perl-io-captureoutput>=1.0801' 'perl>=5.4.50')
makedepends=()
url='http://search.cpan.org/dist/Devel-CheckLib'
source=('http://search.cpan.org/CPAN/authors/id/M/MA/MATTN/Devel-CheckLib-1.01.tar.gz')
md5sums=('15a68944b5a41d7a3c37d2ca365a79dc')
sha512sums=('9d79d8a7dfb044284f1ba7b248c1d61ef1b6e46a63088ebf65e23fd29ccd34020238a86c0eabec18ea54561eeaf043fe45039f903bebfb186f3ccb839416393a')
_distdir="Devel-CheckLib-1.01"

build() {
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""                 \
      PERL_AUTOINSTALL=--skipdeps                            \
      PERL_MM_OPT="INSTALLDIRS=vendor DESTDIR='$pkgdir'"     \
      PERL_MB_OPT="--installdirs vendor --destdir '$pkgdir'" \
      MODULEBUILDRC=/dev/null

    cd "$srcdir/$_distdir"
    /usr/bin/perl Makefile.PL
    make
  )
}

check() {
  cd "$srcdir/$_distdir"
  ( export PERL_MM_USE_DEFAULT=1 PERL5LIB=""
    make test
  )
}

package() {
  cd "$srcdir/$_distdir"
  make install
  find "$pkgdir" -name .packlist -o -name perllocal.pod -delete
}

# Local Variables:
# mode: shell-script
# sh-basic-offset: 2
# End:
# vim:set ts=2 sw=2 et:
