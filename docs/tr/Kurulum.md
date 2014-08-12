Git'in Kurulumu  ![][1]
===============

Gelin Git'i kullanmaya başlayalım. Her şeyden önce, Git'i kurmanız gerekiyor. Bunu iki başlıca biçimde gerçekleştirebilirsiniz: kaynak kodundan ya da platformunuz için halihazırda varolan paketi kullanarak kurabilirsiniz.

###Kaynak Kodundan Kurulum 
 Yapabiliyorsanız, Git'i kaynak kodundan kurmak kullanışlıdır, çünkü böylece en yeni versiyonunu edinebilirsiniz.
 ----
* Git'i kurmak için, Git'in bağımlı olduğu şu kütüphanelerin sisteminizde bulunması gerekiyor: curl, zlib, openssl, expat, ve libiconv. Örneğin, (Fedora gibi) yum aracına ya da (Debian tabanlı sistemler gibi) apt-get aracına sahip bir sistemdeyseniz bağımlılıkları kurmak için şu komutlardan birini kullanabilirsiniz: 


```bash
	$ yum install curl-devel expat-devel gettext-devel \   openssl-devel zlib-devel
	$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \   libz-dev libssl-dev
```

* Bütün gerekli bağımlılıkları yükledikten sonra Git web sitesinden en son bellek kopyasını edinebilirsiniz:

```bash
	http://git-scm.com/download
``` 
  
* Sonra derleyip kurabilirsiniz:

```bash
    $ tar -zxf git-1.7.2.2.tar.gz
    $ cd git-1.7.2.2
    $ make prefix=/usr/local all
    $ sudo make prefix=/usr/local install
```

* Bu adımdan sonra, Git'teki yeni güncellemeleri Git'in kendisini kullanarak edinebilirsiniz:

```bash
    $ git clone git://git.kernel.org/pub/scm/git/git.git`
```
###Linux'ta Kurulum

* Git'i Linux sisteminize paket kurucu yardımıyla kurmak istiyorsanız, bunu genellikle dağıtımınızla birlikte gelen temel paket yönetim aracıyla yapabilirsiniz. Fedora kullanıcısıysanız, `yum`'u kullanabilirsiniz:

`$ yum install git-core`

* Ubuntu gibi Debian-tabanlı bir sistemdeyseniz, `apt-get`'i kullanabilirsiniz:

`$ apt-get install git`

###Mac'te Kurulum

* Git'i Mac'te kurmak için iki kolay yol vardır. En kolayı, SourceForge sayfasından indirebileceğiniz görsel Git yükleyicisini kullanmaktır.

`http://sourceforge.net/projects/git-osx-installer/`

* Diğer başlıca yol, Git'i [MacPorts](http://www.macports.org) vasıtasıyla kurmaktır. MacPorts halihazırda kurulu bulunuyorsa Git'i şu komutla kurabilirsiniz:

`$ sudo port install git-core +svn +doc +bash_completion +gitweb`

Bütün ek paketleri kurmanız şart değil, ama Git'i Subversion yazılım havuzlarıyla kullanmanız gerekecekse en azından +svn'i edinmelisiniz.

###Windows'ta Kurulum

Git'i Windows'da kurmak oldukça kolaydır.Alt kısımdaki sayfasından indirip çalıştırmanız yeterli:

`http://git-scm.com/download/win`

===========

#### Kaynak : ####
[Pro Git Book](http://git-scm.com/book/tr/)

[1]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/install.png