# Polymer

> Gmolymer, Dev testneti mevcut ama bizde IBC Channel oluşturup katılalım bir nebze.

> Şahsen [benim](https://x.com/Ruesandora0/status/1732454399543234688?s=20) için öenmli bir proje - siz katılmak isterseniz diye paylaşıyorum.

> Günün sonunda rolümüzü alıyoruz. Donanım olarak herhangi bir sunucu yeterli.

> Sorulara hızlı cevap veremeyebilirim hala iyilesmedim ve Can Azerbaycan yolculuğum var 2 gün sonra.

> Topluluk kanalları: [Sohbet Kanalımız](https://t.me/RuesChat) - [Duyurular ve Gelişmeler](https://t.me/RuesAnnouncement) - [Whatsapp](https://whatsapp.com/channel/0029VaBcj7V1dAw1H2KhMk34) - [Polymer Discord](https://discord.gg/nSUdZ7tg)

```console
sudo apt update -y && sudo apt upgrade -y
sudo apt-get install git -y
sudo apt-get install -y ca-certificates curl gnupg
sudo mkdir -p /etc/apt/keyrings

# içersine giriyoruz
sudo nano /etc/apt/sources.list.d/nodesource.list
# alttaki komutu içersine girdiğimiz dosyaya yazıyoruz. (# ile deb arasında boşluk bırakın)
#deb [signed-by=/etc/apt/keyrings/nodesource.gpg] https://deb.nodesource.com/node_ jammy main

sudo apt update -y && sudo apt upgrade -y
sudo apt-get install -y nodejs
```

```console
# polymer kurulum
git clone https://github.com/sarox0987/polymerlab-ibc-app-solidity.git
cd polymerlab-ibc-app-solidity

# just  ve forge kurulumu
curl --proto '=https' --tlsv1.2 -sSf https://just.systems/install.sh | bash -s -- --to /usr/local/bin
curl -L https://foundry.paradigm.xyz | bash
source /root/.bashrc
foundryup
forge build
```

<h1 align="center"> Cüzdan ve API key hazırlığı </h1>

> Poylmer için bir testnet metamask account oluşturun.

> [Buradan](https://www.alchemy.com/faucets/optimism-sepolia) optimism - [Buradan](https://www.alchemy.com/faucets/base-sepolia) base faucet alın.

> Alchemy hesabı [oluşturup](https://dashboard.alchemy.com/apps) apps kısmından Optimism Sepolia ve Base Sepolia App oluşturun.

<img width="1222" alt="Ekran Resmi 2024-03-09 22 26 16" src="https://github.com/ruesandora/Polymer/assets/101149671/b0c470c3-89f8-400f-81ec-e143b40d7349">

```console
# içersine girelim
nano .env
```

> `PRIVATE_KEY_1` = Metamask private keyi

> `OP_ALCHEMY_API_KEY` = Optimism API Key'i (RPC değil)

> `BASE_ALCHEMY_API_KEY` = Base apı Key'i (RPC değil)

> Tırnakların içersine olacak, CTRL X Y enter ile kaydedip çıkıyoruzç

```console
# chanel oluşturma aşaması
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
source ~/.bashrc
nvm install 18
nvm use 18
npm install
just install
just do-it
```
# just yüklenmiyorsa 

önce bu komutu

```
wget -qO - 'https://proget.makedeb.org/debian-feeds/prebuilt-mpr.pub' | gpg --dearmor | sudo tee /usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg 1> /dev/null
echo "deb [arch=all,$(dpkg --print-architecture) signed-by=/usr/share/keyrings/prebuilt-mpr-archive-keyring.gpg] https://proget.makedeb.org prebuilt-mpr $(lsb_release -cs)" | sudo tee /etc/apt/sources.list.d/prebuilt-mpr.list
sudo apt update
``` 

 sonra;

```
sudo apt install just
```

bu komutu girin.


> Akabinde aşağıdaki gibi loglar alacaksınız ve done diyecek.

![image](https://github.com/ruesandora/Polymer/assets/101149671/4346fe3f-425c-4fe8-bdd8-7aeab5ae7eb8)

> Hata verirse, `npx hardhat clean` ve `just do-it` tekrar çalıştır.

> Ekran görüntünü #proof kanalına discordda at ve devs rolünüzü alın.

