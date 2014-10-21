# Git'in Temelleri  ![][1]   


### Bir Git Yazılım Havuzu Edinmek
Git projesi edinmenin 2 yolu vardır. 
 1. Kendi lokalinizde var olan projelerinizi Git'e eklemek,
 2. Belli bir sunucuda var olan Git projesini klonlamak.

#### 1. Var olan Bir Klasörde Yazılım Havuzu Oluşturmak

* komutu yeni bir Git depo oluşturur. Bir Git depo için varolan, sürüm bilgisi olmayan proje dönüştürmek veya yeni boş bir depo başlatmak için kullanılabilir. Sadece bir kere kullanılır her zaman yeni depo oluşturmak anlamsız olur yani, `.git` gizli alt dizin oluşturur.
```bash
 git init
``` 
* Bu komutu çalıştırarak belirtilen bir dizinde yeni bir depo oluşturur, fakat icinde `.git` iceren bos bir dizin oluşturur.
```bash
git init Klasör-İsimi
```

* Var olan dosyalarınızı sürüm kontrolüne eklemek istiyorsanız, o dosyaları belirleyip kayıt altına aldığınız birkaç git komutuyla gerçekleştirebilirsiniz:
```bash
git add *
git add README.md
git commit -m "kayıt değişiklik mesajı"
```
şimdi artık `.git` uzantılı klasörümüzde bizim yeni kayıtlarımız bulunuyor.

#### 2. Var olan Bir Yazılım Havuzunu Klonlamak

* Var olan bir Git projesini klonlamak istiyorsanız ve ya katkıda bulunmak istediğiniz bir projeyi kendi lokalinize klonlamak ve geliştirmek için gerekli git anahtarı `git clone`. Bu anahtar projenin tüm verilerini bile klonluyor versiyonlar tarihçeler vb.
```bash
git clone url
```

--------

[önceki](https://github.com/paufsc/journey-to-git/blob/master/docs/tr/Yapilandirma.md)|[sonraki](https://github.com/paufsc/journey-to-git/blob/master/docs/tr/)
---|---

[1]: https://github.com/paufsc/journey-to-git/blob/master/assets/img/tutorial.png
[1]: https://github.com/smehemmed/journey-to-git/blob/master/assets/img/tutorial.png