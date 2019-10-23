# guide-to-testnet-v0.1.0
EVEN testnet guide

[English Guide](https://github.com/evenfound/guide-to-testnet-v0.1.0#english-guide)

[Инструкция на русском](https://github.com/evenfound/guide-to-testnet-v0.1.0#инструкция-на-русском)
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
