#Git Yapılandırma ![][1]

####Kimliğiniz

Git'i yapılandırmasına başlarken yapmanız gereken ilk şey adınızı ve e-posta adresinizi ayarlamaktır. Bunun önemli olmasının nedeni her bir Git kaydının bu bilgiyi kullanıyor olması ve bu bilgiler ile yaptığınız kaytlarınızı kayıt altına tutar.

```bash
    $ git config --global user.name "Pamukkale University Free Software Community"
    $ git config --global user.email "paugithub@gmail.com"
```

Bu yapılandırmayı yani, `--global` seçeneğini kullandığınızda bunu bir kez yapmanız yeterli olacaktır, çünkü Git, o sistemde yapacağınız her işlem için bu bilgileri kullanacaktır. İsmi ya da e-posta adresini projeden projeye değiştirmek isterseniz, komutu değişiklik yapmak istediğiniz proje klasörünün içinde `--global` seçeneği olmadan çalıştırabilirsiniz.

####Ayarlarınızı Gözden Geçirmek

Ayarlarınızı gözden geçirmek isterseniz, için `git config --list` komutunu kullanabilirsiniz.

*Example:*

```bash
➜  journey-to-git git:(master) ✗ git config --list 
user.name=paufsc
user.email=paugithub@gmail.com
core.repositoryformatversion=0
core.filemode=true
core.bare=false
core.logallrefupdates=true
remote.origin.fetch=+refs/heads/*:refs/remotes/origin/*
remote.origin.url=https://github.com/smehemmed/journey-to-git.git
branch.master.remote=origin
branch.master.merge=refs/heads/master
```

* `git config <secenek>` komutunu kullanarak git'in farklı secenekli ayarlarını görüntüleye bilirsiniz:


```bash
    $ git config user.name
    Pamukkale Ozgur Yazilim Toplulugu
```
####SSH Key

Yeni SSH anahtarı oluşturalım, 

* öncelikle:

```bash
    $ ssh-keygen -t rsa -C "your_email@example.com"
    # Creates a new ssh key, using the provided email as a label
    # Generating public/private rsa key pair.
    # Enter file in which to save the key (/home/you/.ssh/id_rsa):
```
* Sonra, bir parola girmeniz istenir.

```bash
    Enter passphrase (empty for no passphrase): [Type a passphrase]
    # Enter same passphrase again: [Type passphrase again]
```

* Böyle bir ekran ile karşılaşmanız lazim

```bash
    Your identification has been saved in /home/you/.ssh/id_rsa.
    # Your public key has been saved in /home/you/.ssh/id_rsa.pub.
    # The key fingerprint is:
    # 01:0f:f4:3b:ca:85:d6:17:a1:7d:f0:68:9d:f0:a2:db your_email@example.com
```

* Sonra, `ssh-agent`'e yeni anahtarı ekleyin:

```bash
    # start the ssh-agent in the background
    $ eval "$(ssh-agent -s)"
    # Agent pid 59566
    $ ssh-add ~/.ssh/id_rsa
```

* Oluşturduğumuz anahtarı kopyalamak için aşağıdaki kodu çalıştırın.

```bash
    $ sudo apt-get install xclip
    # Downloads and installs xclip. If you don't have `apt-get`, you might need to use another installer (like `yum`)
    $ xclip -sel clip < ~/.ssh/id_rsa.pub
    # Copies the contents of the id_rsa.pub file to your clipboard
```

* Alternatif olarak,
> *bu dizine bulunan `~/.ssh/id_rsa.pub` dosyasını açıp ve manuel olarak içeriğini kopyalamayabilirsiniz.*

* Şimdi anahtarı kopyaladıktan sonra, GitHub hesabımıza ekliyelim:

* Aşağıdaki adımları uygulayalım  

1. Sağ üst köşesindeki kullanıcı çubuğunda [Ayarlar butonu](https://github.com/settings/profile) ![][2]

2. Sol kısımda [SSH Key](https://github.com/settings/ssh) seçeneğini secelim ![][3]

3. Add SSH seçeneyine tıklayalım   ![][4]

4. Başlık alanında, yeni anahtar için açıklayıcı bir etiket ekleyin. 

5. Boşluk kısmina 'Yapıştır' (`ctrl+v`) SSH Keyi yapıştıralım ![][5]

6. **Add Key**'e tıklayalım ![][6]

7. Github şifrenizi girerek işlemi onaylayın.

#### Her şeyi test edelim şimdi;

Şimdi Github hesabımız ile bağlatı kurmaya çalışalım ve daha önce oluşturduğunuz parola oldu şifrenizi kullanarak yapaçaksınız.

* Termineli açalım (`ctrl+alt+T`);

```bash
    $ ssh -T git@github.com
    # Attempts to ssh to github
```
Böyle hata mesajı ile karşılaşabilirsiniz!

```bash
    ...
    Agent admitted failure to sign using the key.
    debug1: No more authentication methods to try.
    Permission denied (publickey).
```
* Karşılaşmanız gereken mesaj böyle olması gerekiyor ve `yes` yazarak bu adımı bitirebilirsiniz.

```bash
    The authenticity of host 'github.com (207.97.227.239)' can't be established.
    # RSA key fingerprint is 16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48.
    # Are you sure you want to continue connecting (yes/no)?
```
* Son olarak;

```bash
    Hi username! You've successfully authenticated, but GitHub does not
    # provide shell access.
```

===========

[önceki](https://github.com/paufsc/journey-to-git/blob/master/docs/tr/Kurulum.md)|[sonraki]()
---|---

  [1]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/setting.png
  [2]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/ssh1.png
  [3]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/ssh2.png
  [4]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/ssh3.png
  [5]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/ssh4.png
  [6]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/ssh5.png