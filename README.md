<h1 align="center">Paloma-Node-TR</h1>

![paloma](https://user-images.githubusercontent.com/101149671/173926483-33d00bf3-861e-4e30-9339-e04360cbd16b.png)


Paloma Projesi Türkçe Kaynaklar


Gereksinimler (minimum):
```
2 vcpu 
16 ram 
100 gb
```

<h1 align="center">Paloma Node Kurulumu ve Cüzdan oluşturma</h1>

# Cüzdan oluşturduktan sonra dolduruyoruz: [Form](https://docs.google.com/forms/d/e/1FAIpQLSdSviH22JzZ70wcKd1FTevPOiab7g4fyDA3WphKVpYlKBiqkQ/viewform) 

# Go Kurulumu

  
    cd $HOME
    wget -O go1.17.1.linux-amd64.tar.gz https://golang.org/dl/go1.17.1.linux-amd64.tar.gz
    rm -rf /usr/local/go && tar -C /usr/local -xzf go1.17.1.linux-amd64.tar.gz && rm go1.17.1.linux-amd64.tar.gz
    echo 'export GOROOT=/usr/local/go' >> $HOME/.bash_profile
    echo 'export GOPATH=$HOME/go' >> $HOME/.bash_profile
    echo 'export GO111MODULE=on' >> $HOME/.bash_profile
    echo 'export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin' >> $HOME/.bash_profile && . $HOME/.bash_profile
    go version


# Kütüphane Kurulumu

   

    cd $HOME
    sudo apt update
    sudo apt install make clang pkg-config libssl-dev build-essential git jq ncdu bsdmainutils -y < "/dev/null"



# Paloma Kurulumu & Cüzdan Alma


    wget -O - https://github.com/palomachain/paloma/releases/download/v0.1.0-alpha/paloma_0.1.0-alpha_Linux_x86_64v3.tar.gz | \
    sudo tar -C /usr/local/bin -xvzf - palomad
    sudo chmod +x /usr/local/bin/palomad
    sudo wget -P /usr/lib https://github.com/CosmWasm/wasmvm/raw/main/api/libwasmvm.x86_64.so
    //<moniker-isminiz> burayı degiştirin
    MONIKER="<moniker-isminiz>"
    palomad init "$MONIKER"


# Default Ayarlar

   
    wget -O .paloma/config/genesis.json https://raw.githubusercontent.com/palomachain/testnet/master/livia/genesis.json
    wget -O .paloma/config/addrbook.json https://raw.githubusercontent.com/palomachain/testnet/master/livia/addrbook.json

    
# Cüzdan Oluşturma
   
    // <moniker-ismi> SİLİP İSMİNİZİ GİRİN
    VALIDATOR=<moniker-ismi>
    palomad keys add "$VALIDATOR"

Cüzdanınızı kaydedin ve Testnete başvurun.. 


# Paloma Tesnet

17 -24 Haziran 

15-22 Temmuz

12-19 ağustos

16-23 Eylül

# DAHA FAZLA SORUNUZ VARSA PALOMA TÜRKİYE TELEGRAM GRUBU:

[Telegram](https://t.me/PalomaTurkish)
