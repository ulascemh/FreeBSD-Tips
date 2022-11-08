# sysrc Programı ve rc.d Scripti

**sysrc** programı toplu ve güvenli şekilde rc scriptini düzenlemeyi sağlar.

`sysrc -a` komutu ile varsayılan olmayan tüm satırları yazdırabiliriz.

`sysrc -x __deger_adi__` komutu ile bir satırı silebiliriz.

## /etc/rc.d Komutları

### rc_startmsgs

Multiuser olarak başlarken her başlayan deamon için mesaj yazar bu komutla o mesajları kapatabiliriz.

```sh
rc_startmsgs="NO"
```

### syslog_enable="YES"

### sshd_enable="NO"

### hostname=""

### pf_enable="NO"

Enable Packet Filter

### keymap=

### blanktime="300"

Belirli saniye sonra ekranı karartma

### Font Ayarları

```sh
font8x16="NO"
font8x14="NO"
font8x8="YES"
```

### Mouse Ayarları

```sh
mouse_enable="NO"
mouse_type="AUTO"
```

### Çözünürlük Kontrolü

```sh
allscreens_flags=""
# Tüm olası parametreler için man vidcontrol
```

## Servislerin Kontrolleri

`service __servis_adi__ __komut__`

* Olası komutlar
  * start *servisi başlat*
  * stop *servisi durdur*
  * restart *servisi durdur ve tekrar başlat*
  * rcvar *İlgili servise ait rc.d içerisindeki satırları yazır.*
  * enabled *Eğer servis aktif ise true döddürür.*
  * describe *Servisin açıklamasını yazdırır.*
  * Ekstra komutlar
    * Servise özel komutlar olabilir.
    * status *Servis çalışır haldemi onu belirtir.*

## Minik Notlar

`shutdown`, `halt`, `reboot` komutları kullanıldığında sistem /etc/rc.shutdown scriptini çalıştırır. Bu scriptte rc.d scriptini stop argümanı ile çağırır.