# TAR

Tape Archiver'in kısaltılmışıdır.

FreeBSD **bsdtar** adındaki tar versiyonunu kullanır.

## Yedek Oluşturma

`-c` create mode

```sh
tar -c /home /var
# home ve var klasörlerindeki herşeyi yedekler.
```

## Arşiv içeriğini Listeleme

`-t` list mode

```sh
tar -t /home/test.tar
```

## Yedeklerden dosyaları çıkarma

```sh
cd /home/test
tar -x etc
```

## Sadece dosya yedeklemek için kullanmak

```sh
tar -cf __tar_ismi__.tar /home/test
```

## Sıkıştırma

### XZ Sıkıştırması

`-J` **.txz** olarak sıkıştırır.

### GZIP Sıkıştırması

`-Z` **tar.gz** veya **.tgz** olarak sıkıştırır.

### BZIP Sıkıştırması

`-j` **.tbz** olarak sıkıştırır.