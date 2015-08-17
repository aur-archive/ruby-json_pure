# Maintainer: Jochen Schalanda <jochen+aur@schalanda.name>
# Contributor: Hyacinthe Cartiaux <hyacinthe.cartiaux@free.fr>
# Contributor: Evan Pitstick <nerdx00+Arch AT gmail DOT com>
# Contributor: Daenyth <Daenyth+Arch AT gmail DOT com>
# Contributor: Alexsandr Pavlov <kidoz at mail dot ru>
pkgname=ruby-json_pure
_gemname=${pkgname#ruby-}
pkgver=1.8.1
pkgrel=1
pkgdesc="A Ruby implementation of the JSON specification according to RFC 4627."
arch=('any')
url="http://flori.github.com/json"
license=('GPL')
depends=('ruby')
source=(https://rubygems.org/downloads/${_gemname}-${pkgver}.gem)
noextract=(${_gemname}-${pkgver}.gem)
sha512sums=('f635b127cf6ba4af07b8bd133696021e3f47e41b743d5a874af7481679a7031a2c3c9ae8bddbe7d84ff72c929da1302b9cf863a075fda6aeca08688d2032a282')

package() {
  cd "${srcdir}"

  local _gemdir="$(ruby -rubygems -e'puts Gem.default_dir')"
  gem install --no-user-install --ignore-dependencies -i "${pkgdir}${_gemdir}" ${_gemname}-${pkgver}.gem
}
