# Maintainer: Aliasbody <aliasbody@gmail.com>
pkgname=javafx-sdk2.1
pkgver=2.1b21
pkgrel=1
pkgdesc="JavaFX is designed to provide a lightweight, hardware-accelerated Java UI platform for enterprise business applications"
url="http://javafx.com/"
arch=('x86_64' 'i686')
license=('Oracle Technology Network Licence')
depends=('java-runtime')
provides=('javafxpackager')
source=("https://dl.dropbox.com/s/i3hvti0nztsxjom/javafx_sdk-2_1_0-fcs-b21-linux-i586.zip")

package() { 
	installDir="$pkgdir/usr/lib/jvm/$pkgname"
	appDir=javafx-sdk2.1.0
	
	# Creates a directory called javafx-sdk2.1 in /usr/lib/jvm
	msg "(1/5) Creating the JavaFX folder"
	mkdir -p $installDir
	
	# Copying all the files from the original folder to the new one
	msg "(2/5) Moving Files"
	cp -R $appDir/* $installDir
	
	# Creating the symlinks and the executables
	msg "(3/3) Creating the Symlink"
	mkdir -p $pkgdir/usr/bin/
	
	chmod u+x $installDir/bin/javafxpackager
	ln -s $installDir/bin/javafxpackager $pkgdir/usr/bin/javafxpackager
}

md5sums=('55977c12b5c8f654586130239805318a')