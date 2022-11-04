# /boot/loader.conf

*Boot esnasında çalışan ilk script.*

## Örnekler

### boot_verbose

Boot esnasında çıkan bilgi yazılarının tam detaylı olmasını sağlar. *Debug yaparken hayat kurtarabilir.*

```sh
boot_verbose="NO"
```

### autoboot_delay

Boot menüsünün seçim için kaç saniye bekleyeceğini belirler.

```sh
autoboot_delay="10"
```

### beastie_disable

Seçim ekranındaki ASCII resminin gösterilmesini ayarlar. *YES olursa çıkmaz.*

```sh
beastie_disable="NO"
```

### loader_logo

Seçim ekranında çıkacak logoyu belirler.

```sh
loader_logo="fbsdbw"
loader_logo="beastiebw"
loader_logo="beastie"
loader_logo="none"
```



## Minik Notlar

- loader.conf işlemlerini tamamladıktan sonra `/etc/rc.d` scripti çalışmaya başlar.