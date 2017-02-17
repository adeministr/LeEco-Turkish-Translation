# LeEco Turkish Translation - LeEco Türkçe Dil Desteği
LeEco (LeTv) cihazlarına ait uygulama romların Türkçe'ye çevrilmesi için oluşturulmuş projedir. MTK ve Snapdragon uygulamaları da konulmuştur. İsteğiniz romların yapımcılarına bu reponun adresini verip Türkçe dil desteği isteyebilirsiniz.

İlgili uygulamaların çevirileri kendi içlerindeki /res/values-tr/ klasörü içerisindeki strings.xml, plurals.xml dir. /res/ klasörünün içerisinde values-tr klasörünü içerenler Türkçe'leştirilmiştir. values veya values-en-rUS olanlar Türkçe'leştirilmemiş, her iki klasör bulunanlar da kontrol amaçlı konulmuştur.

Çevirilerinizi Notepad++ ile yapmanız Türkçe karakterlerin doğru görüntülenmesi ve kodları renklendirdiği için hata yapma olasılığınızı azaltma açısından önemlidir.

Yaptığınız çalışmaları github üzerinden istek göndererek ya da http://forum.turkdevs.com/konu/leeco-turkce-ceviri-ve-dil-destegi-projesi-ana-basligi.12125/ adresine gönderek ya da ademyuce(kuyruklu a)gimeyl nokta com adresine gönderebilirsiniz. Yapılan çeviriler isim ya da kod adlarıyla paylaşılacaktır.


#Çeviri Yaparken Dikkat Edilmesi Gerekenler:

* Çeviri yaparken mutlaka işaretlere dikkat ediyoruz. Orjinal yazılış/kodlama biçimini değiştirmiyoruz.
<string name="example">Çeviri</string> Yandaki gibi sadece > ve < arasına yazıyoruz yani Çeviri olan yere yazıyoruz aksi halde uygulama derlenmez hata verir. Örneğin: <string name="cancel">İptal</string ya da <string name="cancel">İptal string> hata verecektir.

* dil dosyaları xml olarak kodlanmıştır. xml'e ait özel işaretlerden kullanmanız gerekiyorsa " " içerisine yazılmalıdır:
<string name="example">Türkiye'nin</string> hata verecektir. Doğrusu: <string name="example">"Türkiye'nin"</string> olacaktır.

* yine en çok dikkat edilmesi gereken uygulamayı yazanın uygulamayı kişiselleştirebilmek için bazı değerleri ve varsayılan ayarları dil dosyasına gömdüklerinden bu alanların kesinlikle dokunulmaması gerektiğidir; eğer bu alanlar da tercüme edilirse uygulamada o alana girince uygulama kapanacaktır ya da ilgili alanlar çalışmayacaktır. Örnek:
    <string name="app_name">Yeniden Başlatma Ayarları</string>
    <string name="reboot_label">Yeniden Başlat</string>
    <string name="reboot_recovery_label">Recovery Modu</string>
    <string name="reboot_bootloader_label">Bootloader Modu</string>
    <string name="shutdown_label">Kapat</string>
    <string name="reboot_dialog_message">Telefonunuz yeniden başlatılacak.</string>
    <string name="reboot_dialog_title">Yeniden başlat</string>
    <string name="reboot_recovery_dialog_title">Recovery Modu</string>
    <string name="reboot_recovery_dialog_message">Telefonunuz Recovery modunda başlatılacak.</string>
    <string name="reboot_bootloader_dialog_title">Bootloader Modu</string>
    <string name="reboot_bootloader_dialog_message">Telefonunuz Bootloader modunda başlatılacak.</string>
    <string name="shutdown_dialog_title">Kapat</string>
    <string name="shutdown_dialog_message">Telefonunuz Kapatılacak.</string>
    <string name="reboot_command">reboot</string>
    <string name="reboot_recovery_command">reboot recovery</string>
    <string name="reboot_bootloader_command">reboot bootloader</string>
    <string name="shutdown_command">reboot -p</string>
    
    Yukarıda görüldüğü gibi sonu _name, _label, _message, _entry, _title vb ile bitenler tercüme edilebilirken sonu _command ile bitenler direkt olarak komutun kendisidir. Tercüme edildiği takdirde ilgili alan ya çalışmayacak ya da program hata verecektir.
    
    Benzer problemler _default, _value vb için de geçerlidir.
    
* Uygulamanın konusu doğrultusunda çeviri yapılması çevirilerin doğruluğu açısından önem taşımaktadır.
