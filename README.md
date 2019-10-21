# guide-to-testnet-v0.1.0
EVEN testnet guide

[English Guide](https://github.com/evenfound/guide-to-testnet-v0.1.0#english-guide)

[Инструкция на русском](https://github.com/evenfound/guide-to-testnet-v0.1.0#инструкция-на-русском)
## English Guide
## Инструкция на русском
### Установка 

1. Разархивировать файлы .zip

2. Создать папку ~/even-data (В windows C:/Users/**username**/even-data)

3. Перенести even, evenctl, ipfs в директорию even-data

4. Вызвать командную строку. В переменную среду ос добавить в PATH  полный путь к even-data:

`cd C:/Users/**username**/even-data`

5. Инициализировать конфигурации 

`even init --verbose`

После выполнения этой команды в директории $HOME/.config/even появляются конфигурационные файлы 

6. Для запуска ноды нужны выполнять команду

`even start --testnet [--verbose]`


### Работа с пирами 

1. Получить свой идентификатор 

`evenctl peer id`

2. Получить список пиров в сети 

`evenctl peer list`

### Создание кошелька 

1. Ввести в командную строку:

`evenctl wallet create`

2. Создать пароль и мнемоническую фразу (когда вы вводите пароль, символы в командной строке не отображаются):

`Enter the private passphrase for your new wallet: 
Please confirm the phrase you just entered: 
Do you have an existing mnemonic phrase you want to use? (n/no/y/yes) [no]: n
Do you have an existing wallet seed phrase you want to use? (n/no/y/yes) [no]: n
Your wallet generation mnemonic phrase is`

3. После выполнение этой команды можно сразу перейти на генерацию аккаунта . Но для этого нужно сперва разблокировать 
аккаунт с паролем который указали при создании кошелька. Введите:

`evenctl wallet unlock`

и укажите ваш пароль 

`Provide existing wallet private passphrase: `

4. Создание аккаунта:

`evenctl wallet nextaccount`

скопируйте адрес вашего кошелька

5. После генерации аккаунтов можно получить баланс 
`evenctl wallet balance -l **адрес вашего кошелька**`

2019/10/11 14:07:45 Call failed [Network: ]: wallet has no funds

и отправить платежную транзакцию 

$ evenctl wallet tx pay  -t mm65wXwTEKyc2vGksSuTTzJBu54AuS2yN7 -f mm65wXwTEKyc2vGksSuTTzJBu54AuS2yN7 -v 1000


### Работа с папками 

Получение всех файлов в папке  shared / ledger

$ evenctl folder list shared
2019/10/11 14:11:34 shared:
/home/yuri/.config/even/shared/GENESIS_a5214607c0b7f7866797691371de2e40133e8c56f5a2500ba877b9be4fe22f5d_1559652360000000000

Добавление файла в директорию 

$ evenctl folder write shared  -f /bin/bash
2019/10/11 14:14:17 QmYtMhLMFzHV6VhkxjBwQqGMWwF8vcgUb7GuNRaYB91yLf
