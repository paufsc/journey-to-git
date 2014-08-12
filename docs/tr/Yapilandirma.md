##Git Yapılandırma ![][1]

####Kimliğiniz

Git'i kurduğunuzda yapmanız gereken ilk şey adınızı ve e-posta adresinizi ayarlamaktır. Bunun önemli olmasının nedeni her bir Git kaydının bu bilgiyi kullanıyor olması ve bu bilgilerin dolaşıma soktuğunuz kayıtlara değişmez biçimde işlenmesidir.

```bash
    $ git config --global user.name "John Doe"
    $ git config --global user.email johndoe@example.com
```

Yinelemek gerekirse, `--global` seçeneğini kullandığınızda bunu bir kez yapmanız yeterli olacaktır, çünkü Git, o sistemde yapacağınız her işlem için bu bilgileri kullanacaktır. İsmi ya da e-posta adresini projeden projeye değiştirmek isterseniz, komutu değişiklik yapmak istediğiniz proje klasörünün içinde `--global` seçeneği olmadan çalıştırabilirsiniz.


####Kaynak
   * [Atlassian Git Tutorials](https://www.atlassian.com/git/)

[1]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/setting.png