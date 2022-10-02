# Wormholes Testnet Rehberi

![Wormholes - Testnet](https://user-images.githubusercontent.com/107190154/193325968-3f3954f0-e736-423e-9153-7f3aff500868.gif)

### Sistem Gereksinimleri (Minimum)

![image](https://user-images.githubusercontent.com/107190154/193319079-00dd8efb-61ed-4dd7-8d74-f7713cccad12.png)

## [Orijinal Doküman](https://www.wormholes.com/docs/Install/run/index.html)

### Not: Private keyinizi başında `0x` olmadan yazın. Aksi halde yeni bir key oluşturuyor.
### Not: Ekip bu sorunu son güncelleme ile düzelttiklerini açıkladılar.

**Örnek: 0x123z987agwhwtd6tyuahpo98786atdfaAUGIFT yerine 123z987agwhwtd6tyuahpo98786atdfaAUGIFT yazmalısınız.**

## Daha evvel kurup güncelleme yapmak isteyenler için
```
wget -O wormholes.sh https://raw.githubusercontent.com/brsbrc/Testnetler-ve-Rehberler/main/Wormholes/wormholes.sh && chmod +x wormholes.sh && ./wormholes.sh
```

### Kurulum için 
```
sudo apt-get update && apt-get upgrade -y
```
```
cd /root
```
```
sudo apt install docker.io
```
```
sudo systemctl enable --now docker
```
> Private keyinizi başında `0x` olmadan yazın.
```
wget -O wormholes.sh https://raw.githubusercontent.com/brsbrc/Testnetler-ve-Rehberler/main/Wormholes/wormholes.sh && chmod +x wormholes.sh && ./wormholes.sh
```

### Sizden Kurulum sırasında private key isteyecek, peki bu keye nasıl ulaşabilirsiniz.

### Şu işarete basalım.
![Ekran görüntüsü 2022-09-30 202147](https://user-images.githubusercontent.com/107190154/193323716-ecd5d453-f3f1-49cd-931a-cc151b63d15b.png)

### Settings Kısmına girelim.
![image](https://user-images.githubusercontent.com/107190154/193324401-133be871-43b4-4ac5-8d9e-c0768f28f2c1.png)

### İşaretlediğim kısma tıklayın ve cüzdan şifrenizi yazın.
![Ekran görüntüsü 2022-09-30 202801](https://user-images.githubusercontent.com/107190154/193324554-fe77ddc7-17ea-4fa3-8e65-39d81b5e93ca.png)

### Karşınıza çıkan sizin private keyiniz. Scriptte sizden istenen yere private keyinizi başında `0x` olmadan yazın.
![Ekran görüntüsü 2022-09-30 203010](https://user-images.githubusercontent.com/107190154/193324930-e56d9ccb-b5b4-4c87-8499-38982dbe81ac.png)


## Bazı Komutlar

### Bağlantı Durumu İçin
```
curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"net_peerCount","id":1}' http://127.0.0.1:8545
```

### Blok Kontrol İçin
```
curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"eth_blockNumber","id":1}' http://127.0.0.1:8545
```

### Bakiye Durumu Öğrenme
> cüzdanadresiniziyazın kısmına kendi adresinizi yazın.
```
curl -X POST -H 'Content-Type:application/json' --data '{"jsonrpc":"2.0","method":"eth_getBalance","params":["cüzdanadresiniziyazın","pending"],"id":1}' http://127.0.0.1:8545
```

## Node Kurduk şimdi şu adrese gidelim stake işlemini yapalım: https://www.limino.com/#/wallet

### Şu işarete basalım.
![Ekran görüntüsü 2022-09-30 202147](https://user-images.githubusercontent.com/107190154/193323716-ecd5d453-f3f1-49cd-931a-cc151b63d15b.png)

### `become a validator` kısmına girelim.

![Ekran görüntüsü 2022-09-30 202320](https://user-images.githubusercontent.com/107190154/193323898-b09a073f-8ff3-4a0b-a991-f63086818616.png)

### Stake işlemini Gerçekleştirelim.
> Minimum 70000 erb stake etmelisiniz.
![image](https://user-images.githubusercontent.com/107190154/193324020-c5330cd3-00ba-4fc6-884c-3f8b9195fc6f.png)

## [Explorer](https://www.wormholesscan.com/#/)

### Örneğin benim cüzdanım:

![image](https://user-images.githubusercontent.com/107190154/193441259-d6612456-a998-44f4-be81-65813df4f431.png)

### Şu an yani 02.10.2022 - saat 09.35 itibarıyla bulunan validator sayısı --->> 336

![image](https://user-images.githubusercontent.com/107190154/193441277-2d618aa5-49a6-4641-b126-6867116c060c.png)

### Hata ya da eksik varsa PR atabilirsiniz...

## Sorularınız için: https://t.me/NotitiaGroup