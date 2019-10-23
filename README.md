# guide-to-testnet-v0.1.0
EVEN testnet guide

Windows:

[English Guide](https://github.com/evenfound/guide-to-testnet-v0.1.0#english-guide)

[Инструкция на русском](https://github.com/evenfound/guide-to-testnet-v0.1.0#инструкция-на-русском)

[Guide Français](https://github.com/evenfound/guide-to-testnet-v0.1.0#guide-français) 

Linux:

[English Guide, Linux](https://github.com/evenfound/guide-to-testnet-v0.1.0#english-guide-linux)

# Windows
## English Guide
### Installation 

[Video guide](https://www.youtube.com/watch?v=X8l4rk6cq3s)

1. [Download installation files](https://evenfound.org/product/download). Unzip .zip files

2. Create a directory ~/even-data (for Windows C:/Users/**username**/even-data)

3. Copy **even, evenctl, ipfs** to the **even-data** directory

4. Open command line (Win+R shortcut, type "cmd", press "Enter"). Go to directory **even-data**:

`cd C:/Users/username/even-data`

5. Initialize Configurations

`even init --verbose`

After executing this command, the configuration files appear in the $ HOME/.config/even directory.

6. To start a node, you need to run the command

`even start --testnet`

### Peers 

1. Open command line (Win+R, cmd). Go to directory and get your node ID

`cd C:/Users/username/even-data`

`evenctl peer id`

2. Get a list of peers online

`evenctl peer list`

### Wallet Creation

1. Enter in the command line:

`evenctl wallet create`

2. Create a password and a mnemonic phrase (when you enter a password, characters on the command line are not displayed):

`Enter the private passphrase for your new wallet: `

`Please confirm the phrase you just entered: `

`Do you have an existing mnemonic phrase you want to use? (n/no/y/yes) [no]: n`

`Do you have an existing wallet seed phrase you want to use? (n/no/y/yes) [no]: n`

`Your wallet generation mnemonic phrase is`

3. After executing this command, you can generate a wallet account. But for this you need to unlock
account with the password that was specified when creating the wallet. Enter:

`evenctl wallet unlock`

and enter your password

`Provide existing wallet private passphrase: `

4. Create an account

`evenctl wallet nextaccount`

and copy and safe an address of your wallet which you see now in command line

5. Get your balance after wallet generation

`evenctl wallet balance -l your_wallet_address`

To top up the balance of your test wallet, send the wallet address to the chat https://t.me/eventalk1 or to [Issues](https://github.com/evenfound/guide-to-testnet-v0.1.0/issues). 

6. Submit Payment Transaction

`evenctl wallet tx pay  -t recepient_wallet_address -f your_wallet_address -v 1000`

### Directories 

1. List all files in a folder  shared / ledger

`evenctl folder list shared`

2. Add a file to a directory

`evenctl folder write shared  -f /bin/bash`

## Инструкция на русском
### Установка 

[Видео](https://www.youtube.com/watch?v=s6abdpFdm-I)

1. [Загрузить файлы установки](https://evenfound.org/ru/product/download). Разархивировать файлы .zip

2. Создать папку ~/even-data (в Windows C:/Users/**username**/even-data)

3. Перенести even, evenctl, ipfs в директорию even-data

4. Вызвать командную строку (нажмите комбинацию Win+R, введите в открывшемся окне команду "cmd" и нажмите "Ввод"). Перейти в директорию even-data:

`cd C:/Users/username/even-data`

5. Инициализировать конфигурации 

`even init --verbose`

После выполнения этой команды в директории $HOME/.config/even появляются конфигурационные файлы. 

6. Для запуска ноды нужно выполнять команду

`even start --testnet`


### Работа с пирами 

1. Вызвать командную строку (Win+R, cmd). Перейти в рабочую директорию и получить свой идентификатор 

`cd C:/Users/username/even-data`

`evenctl peer id`

2. Получить список пиров в сети 

`evenctl peer list`

### Создание кошелька 

1. Ввести в командную строку:

`evenctl wallet create`

2. Создать пароль и мнемоническую фразу (когда вы вводите пароль, символы в командной строке не отображаются):

`Enter the private passphrase for your new wallet: `

`Please confirm the phrase you just entered: `

`Do you have an existing mnemonic phrase you want to use? (n/no/y/yes) [no]: n`

`Do you have an existing wallet seed phrase you want to use? (n/no/y/yes) [no]: n`

`Your wallet generation mnemonic phrase is`

3. После выполнение этой команды можно сразу перейти к генерации аккаунта . Но для этого нужно сперва разблокировать 
аккаунт с паролем который указали при создании кошелька. Введите:

`evenctl wallet unlock`

и укажите ваш пароль 

`Provide existing wallet private passphrase: `

4. Создание аккаунта:

`evenctl wallet nextaccount`

скопируйте и сохраните адрес вашего кошелька, который появился в командной стоке

5. После генерации аккаунтов можно получить баланс 

`evenctl wallet balance -l адрес_вашего_кошелька`

Чтобы пополнить баланс вашего тестового кошелька, отправьте адрес кошелька в чат https://t.me/eventalk1 или в раздел [Issues](https://github.com/evenfound/guide-to-testnet-v0.1.0/issues). 

6. Отправить платежную транзакцию

`evenctl wallet tx pay  -t адрес_кошелька_получателя -f адрес_вашего_кошелька -v 1000`

### Работа с папками 

1. Получение всех файлов в папке  shared / ledger

`evenctl folder list shared`

2. Добавление файла в директорию 

`evenctl folder write shared  -f /bin/bash`

## Guide Français

### Installation

Guide vidéo

1. [Telecharger le fichier d'installation](https://evenfound.org/ru/product/download). Unzip .zip les fichiers

2. Créez un dossier  ~/even-data (Sur Windows C:/Users/username/even-data)

3. Copier/coller even, evenctl, ipfs dans le dossier even-data 

4. Ouvrir la ligne de commande (raccourcis Win+R, taper "cmd", appuyez sur "Enter"). Entrez dans le dossier even-data:

`cd C:/Users/username/even-data`

5. Débutez la configuration

`even init --verbose`

Après avoir exécuté cette commande , le fichier de configuration apparaît dans le dossier  $ HOME/.config/even 

Pour démarrer un noeud (node) vous devez lancer cette commande

`even start --testnet`

### Peers

1. Ouvrez la ligne de commande (Win+R, cmd). Allez dans les dossiers et obtenez votre “node ID”

`cd C:/Users/username/even-data`
`evenctl peer id`

2. Obtenez une liste des peers online

`evenctl peer list`

### Création du portefeuille

1. Entrez dans la ligne de commande:
`evenctl wallet create`

2. Créez un mot de passe et une phrase de secours (lorsque vous entrez votre mot de passe, la ligne de commande reste vide):

`Enter the private passphrase for your new wallet:

Please confirm the phrase you just entered:

Do you have an existing mnemonic phrase you want to use? (n/no/y/yes) [no]: n

Do you have an existing wallet seed phrase you want to use? (n/no/y/yes) [no]: n

Your wallet generation mnemonic phrase is`

3. Après avoir exécuté ces commandes, vous pouvez créer un portefeuille. Mais pour cela vous avez besoin de déverrouiller votre portefeuille avec le mot de passe précédemment choisis. Entrer:

`evenctl wallet unlock`

puis votre mot de passe

`Provide existing wallet private passphrase:`

4. Créez votre compte

`evenctl wallet nextaccount`

puis copier et sécuriser  l’adresse de votre portefeuille que vous voyez maintenant dans la ligne de commande

5. Regardez votre solde
`evenctl wallet balance -l your_wallet_address`

Pour obtenir des even test rejoignez  https://t.me/eventalk1 

6. Soumettre une transaction

`evenctl wallet tx pay -t recepient_wallet_address -f your_wallet_address -v 1000`


# Linux
## English Guide Linux

### Installation 

1. Make application dir:

	$ cd ~
	$ mkdir even-data

2. Copy even-data.zip to ~/even-data from path where archive downloaded:

	$ cp ./even-data.zip ~/even-data

3. Unzip archive:

	$ cd ~/even-data
	$ unzip even-data.zip 
4. Add ~/even-data to PATH environment value:

	$ PATH=$PATH:~/even-data
	$ export $PATH

	Note: After reboot entered value was lost, that you need to add last two string to ~/.profile using echo >

5. The first initialize daemon is:
	
	$ cd ~/even-data
	$ ./even init --verbose
	
	Note: If initialized successfully, in the $HOME dir will be created /.config/even dir. 
	      If you want reinitialize all configurations (attention: that case will be destroy all early created key-pairs for all you wallets and all you coins!), 
	      you may delete $HOME/.config/even dir.

6. After initialization node daemon ready to work:

	$ ./even start --testnet [--verbose]

### Work with peers

1. Get you node peer:

	$ ./evenctl peer id
	$ QmRGzxoGii5jQDwQRdiEsiiRhHdZL7DJ6Fscy2ZUA95m5S

2. Collate all running network peers:

	$ ./evenctl peer list
	$ QmRGzxoGii5jQDwQRdiEsiiRhHdZL7DJ6Fscy2ZUA95m5S
	$ QmRGzxoGii5jQDwQRdiEsiiRhHdZL7DJ6Fscy2ZUA95m5S
	$ QmRGzxoGii5jQDwQRdiEsiiRhHdZL7DJ6Fscy2ZUA95m5S
	$ QmRGzxoGii5jQDwQRdiEsiiRhHdZL7DJ6Fscy2ZUA95m5S

### Wallet 

1. Create and unlock:

	$ ./evenctl wallet create
	$ Enter the private passphrase for your new wallet: 
	$ Please confirm the phrase you just entered: 
	$ Do you have an existing mnemonic phrase you want to use? (n/no/y/yes) [no]: n
	$ Do you have an existing wallet seed phrase you want to use? (n/no/y/yes) [no]: n
	$ Your wallet generation mnemonic phrase is
	$ ******************************************************************************************
	$ special immense gentle trend trend language glass result wink toddler grain wise

	$ .......................................................................................

	Note: In command process you need enter password and textual seed phrase. Entered phrase we are recommend to save in to private storage.
	       After that command runs you can start account generate. For this action you need unlock wallet with previous entered password first.

	$ ./evenctl wallet unlock
	$ Provide existing wallet private passphrase: 
	$ 2019/10/11 13:56:25 Call completed [Network: testnet]: map[even:unlocked]

2. Generate next (new - look BIP44 issue) account: 
	
	$ ./evenctl wallet nextaccount
	$ 2019/10/11 13:56:29 Call completed [Network: testnet]: map[even:address:"mm65wXwTEKyc2vGksSuTTzJBu54AuS2yN7" ]

3. Balance:

	Note: After account generation you can got wallet balance:

	$ ./evenctl wallet balance -l mm65wXwTEKyc2vGksSuTTzJBu54AuS2yN7
	$ 2019/10/11 14:07:45 Call failed [Network: ]: wallet has no funds
  
  To top up the balance of your test wallet, send the wallet address to the chat https://t.me/eventalk1 or to [Issues](https://github.com/evenfound/guide-to-testnet-v0.1.0/issues). 

...and send payment transaction:

	$ ./evenctl wallet tx pay  -t mm65wXwTEKyc2vGksSuTTzJBu54AuS2yN7 -f mm65wXwTEKyc2vGksSuTTzJBu54AuS2yN7 -v 1000

### Directories maintenance: 

1. Get the shared / ledger directories content:

	$ ./evenctl folder list shared
	$ 2019/10/11 14:11:34 shared:
	$ /home/<user>/.config/even/shared/GENESIS_a5214607c0b7f7866797691371de2e40133e8c56f5a2500ba877b9be4fe22f5d_1559652360000000000

2. Adding new file to directory: 

	$ ./evenctl folder write shared  -f ~/.profile 
	$ 2019/10/11 14:14:17 QmYtMhLMFzHV6VhkxjBwQqGMWwF8vcgUb7GuNRaYB91yLf
