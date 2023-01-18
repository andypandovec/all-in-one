# all-in-one

В данном скрипте есть несколько модулей, которые сильно упростят работу с мультами : 

1. binance : вывод с бинанса на кошельки через api key.
2. transfer : вывод с кошельков на другие кошельки (субакки).
3. swap : покупка / продажа любых монет в любой сети через 1inch.
4. bridge : бридж с любой сети в любую сеть через orbiter.
5. checker : чекер баланса кошелька во всех evm сетях через debank.


------------------------------------------------------------------------------------------

Binance :
1. В файле config.py меняем значения 2 переменных : BINANCE_API_KEY и BINANCE_API_SECRET. Взять их можно в своем аккаунте бинанса.
2. В файл private_keys.txt добавляем адреса кошельков, на которые будем выводить.
3. В файле main.py меняем значения переменных в функции binance(). Названия сетей копируй из закомментированного примера в функции.
4. Раскомментируй функцию main() и функцию binance(), затем запускай файл main.py.

------------------------------------------------------------------------------------------

Transfer :
1. В файл private_keys.txt добавляем приватники кошельков, с которых будем выводить.
2. В файл recepients.txt добавляем адреса кошельков, на которые будем выводить. 1 кошелек = 1 кошелек. Если выводить с 30 кошельков, значит нужно вставить 30 кошельков-получателей.
3. В файле main.py в функции transfer_tokens() меняй значения переменных. Если итоговый AMOUNT_TO_TRANSFER будет меньше значения MIN_AMOUNT, монеты не выведутся.
4. Раскомментируй функцию main() и функцию transfer_tokens(), затем запускай файл main.py.

------------------------------------------------------------------------------------------

Swap :
1. В файл private_keys.txt добавляем приватники кошельков.
2. В файле main.py в функции swap_1inch() меняем значения переменных. В переменных FROM_TOKEN_ADDRESS или TO_TOKEN_ADDRESS оставь '' (пусто), если свапаешь с / на ETH.
3. Раскомментируй функцию main() и функцию swap_1inch(), затем запускай файл main.py.

------------------------------------------------------------------------------------------

Bridge : 
1. В файл private_keys.txt добавляем приватники кошельков.
2. В файле main.py в функции bridge_orbiter() меняем значения переменных.
3. Раскомментируй функцию main() и функцию bridge_orbiter(), затем запускай файл main.py.

------------------------------------------------------------------------------------------

Checker :
1. В файл private_keys.txt добавляем адреса или приватники кошельков.
2. В файле main.py в функции check_balance() меняй значения переменных. MIN_TABLE_AMOUNT = баланс монет выше этого числа в $ эквиваленте будут записаны в таблицу, если меньше, то только в total value. В массиве func написаны названия трех функций : 
- protocols = проверяет закинул ли ты бабки в какой-либо протокол.
- tokens = чекает баланс всех твоих токенов.
- nfts = смотрит все нфт которые у тебя есть во всех сетях. 
3. Чтобы отключить какой-либо модуль из этих трех, нужно закомментировать его в массиве func. Советую отключить nfts, тк он отправляет много запросов и ответ приходится ждать долго. 
4. В файл proxies.txt добавь прокси в таком формате : http://login:password@ip:port . Каждое прокси с новой строки. Чем их больше, тем лучше.
5. Результат будет прописан в терминал и в файл (скрипт сам его создаст) debank.txt.

------------------------------------------------------------------------------------------

Важно : sleeping(X, Y) = спим от Х до Y. 

------------------------------------------------------------------------------------------

Скрипт очень функционален и идеально подходит для работы с фермой мультов. I'm = админ паблика https://t.me/hodlmodeth, отправитель редких гемов в [ [ chat ] ](http://t.me/chathodlmodeth) и главный, но не самый умный кодер чата [ [ code ] ](https://t.me/code_hodlmodeth). Все вопросы по кодингу туда.

Donate (eth / bsc / arbitrum / op) : 0xb7415DB78c886c67DBfB25D3Eb7fcd496dAf9021
