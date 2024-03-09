# Polymer


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

> Akabinde aşağıdaki gibi loglar alacaksınız ve done diyecek.

![image](https://github.com/ruesandora/Polymer/assets/101149671/4346fe3f-425c-4fe8-bdd8-7aeab5ae7eb8)

> Hata verirse, `npx hardhat clean` ve `just do-it` tekrar çalıştır.

> Ekran görüntünü #proof kanalına discordda at ve devs rolünüzü alın.

