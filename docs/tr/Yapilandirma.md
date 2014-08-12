Git Yapılandırma ![][1]

####Kimliğiniz

Git'i kurduğunuzda yapmanız gereken ilk şey adınızı ve e-posta adresinizi ayarlamaktır. Bunun önemli olmasının nedeni her bir Git kaydının bu bilgiyi kullanıyor olması ve bu bilgilerin dolaşıma soktuğunuz kayıtlara değişmez biçimde işlenmesidir.

```bash
    $ git config --global user.name "John Doe"
    $ git config --global user.email johndoe@example.com
```

Yinelemek gerekirse, `--global` seçeneğini kullandığınızda bunu bir kez yapmanız yeterli olacaktır, çünkü Git, o sistemde yapacağınız her işlem için bu bilgileri kullanacaktır. İsmi ya da e-posta adresini projeden projeye değiştirmek isterseniz, komutu değişiklik yapmak istediğiniz proje klasörünün içinde `--global` seçeneği olmadan çalıştırabilirsiniz.

####Ayarlarınızı Gözden Geçirmek

Ayarlarınızı gözden geçirmek isterseniz, Git'in bulabildiği bütün ayarları listelemek için `git config --list` komutunu kullanabilirsiniz.

*Example:*

```bash
➜  journey-to-git git:(master) ✗ git config --list 
user.name=msxiyev
user.email=msxiyev@gmail.com
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
remote.origin.url=https://github.com/smehemmed/journey-to-git.git
branch.master.remote=origin
branch.master.merge=refs/heads/master
```

Bir ayarı birden çok kez görebilirsiniz; bunun nedeni Git'in aynı ayarı değişik dosyalardan (örneğin `etc/gitconfig` ve `~/.gitconfig`'den) okumuş olmasıdır. Bu durumda Git gördüğü her bir tekil ayar için en son bulduğu değeri kullanır.

`git config {ayar}` komutunu kullanarak Git'ten bir ayarın değerini görüntülemesini de isteyebilirsiniz:

```bash
    $ git config user.name
    Pamukkale Ozgur Yazilim Toplulugu
```

----------
####Kaynak
   * [Pro Git Book](http://git-scm.com/book/tr)

[1]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/setting.png