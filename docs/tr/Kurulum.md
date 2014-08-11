Git'in Kurulumu  ![][1]
===============

Gelin Git'i kullanmaya başlayalım. Her şeyden önce, Git'i kurmanız gerekiyor. Bunu iki başlıca biçimde gerçekleştirebilirsiniz: kaynak kodundan ya da platformunuz için halihazırda varolan paketi kullanarak kurabilirsiniz.

###Kaynak Kodundan Kurulum 
 Yapabiliyorsanız, Git'i kaynak kodundan kurmak kullanışlıdır, çünkü böylece en yeni versiyonunu edinebilirsiniz.
 ----
* Git'i kurmak için, Git'in bağımlı olduğu şu kütüphanelerin sisteminizde bulunması gerekiyor: curl, zlib, openssl, expat, ve libiconv. Örneğin, (Fedora gibi) yum aracına ya da (Debian tabanlı sistemler gibi) apt-get aracına sahip bir sistemdeyseniz bağımlılıkları kurmak için şu komutlardan birini kullanabilirsiniz: 


```shell
$ yum install curl-devel expat-devel gettext-devel \   openssl-devel zlib-devel
$ apt-get install libcurl4-gnutls-dev libexpat1-dev gettext \   libz-dev libssl-dev
```

* Bütün gerekli bağımlılıkları yükledikten sonra Git web sitesinden en son bellek kopyasını edinebilirsiniz:

    * `http://git-scm.com/download` 
  
* Sonra derleyip kurabilirsiniz:
```shell
    $ tar -zxf git-1.7.2.2.tar.gz
    $ cd git-1.7.2.2
    $ make prefix=/usr/local all
    $ sudo make prefix=/usr/local install
```
* Bu adımdan sonra, Git'teki yeni güncellemeleri Git'in kendisini kullanarak edinebilirsiniz:

    * `$ git clone git://git.kernel.org/pub/scm/git/git.git`
  
  







[1]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/install.png
  
  http://git-scm.com/download/win windows