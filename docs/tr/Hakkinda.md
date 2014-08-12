### Sürüm Kontrolü Hakkında ###

Sürüm kontrolü nedir ve ne işe yarar? Sürüm kontrolü, bir ya da daha fazla dosya üzerinde yapılan değişiklikleri kaydeden ve daha sonra belirli bir sürüme geri dönebilmenizi sağlayan bir sistemdir. Bu kitaptaki örneklerde yazılım kaynak kod dosyalarının sürüm kontrolünü yapacaksınız, ne var ki gerçekte sürüm kontrolünü neredeyse her türden dosya için kullanabilirsiniz.

Bir grafik ya da web tasarımcısıysanız ve bir görselin ya da tasarımın değişik sürümlerini korumak istiyorsanız (ki muhtemelen bunu yapmak istersiniz), bir Sürüm Kontrol Sistemi (SKS) kullanmanız çok akıllıca olacaktır. SKS, dosyaların ya da bütün projenin geçmişteki belirli bir sürümüne erişmenizi, zaman içinde yapılan değişiklikleri karşılaştırmanızı, soruna neden olan şeyde en son kimin değişiklik yaptığını, belirli bir hatayı kimin, ne zaman sisteme dahil ettiğini ve daha başka pek çok şeyi görebilmenizi sağlar. Öte yandan, SKS kullanmak, bir hata yaptığınızda ya da bazı dosyaları yanlışlıkla sildiğinizde durumu kolayca telâfi etmenize yardımcı olur. Üstelik, bütün bunlar size kayda değer bir ek yük de getirmez.

### Git'in Kısa Bir Tarihçesi ###

Hayattaki pek çok harika şey gibi, Git de bir miktar yaratıcı yıkım ve ateşli tartışmayla başladı. Linux çekirdeği (kernel) oldukça büyük ölçekli bir açık kaynak kodlu yazılım projesidir. Linux çekirdek bakım ve geliştirme yaşam süresinin çoğunda (1991-2002), yazılım değişiklikleri yamalar ve arşiv dosyaları olarak tutulup taşındı. 2002 yılında, Linux çekirdek projesi, BitKeeper adında tescilli bir DSKS kullanmaya başladı.

2005 yılında, Linux çekirdeğini geliştiren toplulukla BitKeeper'ı geliştiren şirket arasındaki ilişki bozuldu ve aracın topluluk tarafından ücretsiz olarak kullanılabilmesi uygulamasına son verildi. Bu, Linux geliştirim topluluğunu (ve özellikle Linux'un yaratıcısı olan Linus Torvalds'ı) BitKeeper'ı kullanırken aldıkları derslerden yola çıkarak kendi araçlarını geliştirme konusunda harekete geçirdi. Yeni sistemin hedeflerinden bazıları şunlardı:

   * Hız
   * Basit tasarım
   * Çizgisel olmayan geliştirim için güçlü destek (binlerce paralel dal (branch))
   * Bütünüyle dağıtık olma
   * Linux çekirdeği gibi büyük projelerle verimli biçimde başa çıkabilme (hız ve veri boyutu)

2005'teki doğumundan beri, Git kullanım kolaylıklarını geliştirebilmek için evrilip olgunlaştı, ama yine de bu niteliklerini korudu. Git, inanılmaz ölçüde hızlı, büyük ölçekli projelerde alabildiğine verimli ve çizgisel olmayan geliştirim (bkz. 3. Bölüm) için inanılmaz bir dallanma (branching) sistemine sahip.

===========

|[sonraki](https://github.com/paufsc/journey-to-git/blob/master/docs/tr/Kurulum.md)
-----|-----
