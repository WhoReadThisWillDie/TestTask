# Тестовое задание для курса по бэкенд-разработке на Kotlin

Решение написано на Java. В папке StockExchange хранятся классы, отвественные за логику биржи. 
В файле Main прописан только вывод текстового меню, а так же вызов необходимых методов из классов.

## Классы

### Wallet
Абстрактный класс, от которого наследуются классы User и Terminal. Хранит баланс кошелька в HashMap, 
так же имеет методы пополнения/списания определённой валюты.

### User
Почти ничем не отличается от класса Wallet, имеет лишь один доп. метод, который выводит баланс кошелька пользователя в консоль

### Terminal
Хранит ещё один HashMap, в котором прописаны курсы обмена валютных пар. При вызове метода exchange обновляет
собственный баланс, а так же баланс пользователя. Так же в методе обработка краевых случаев, которые могут возникнуть при обмене.
После завершения обмена вызывается метод updateExchangeRates, который обновляет обменные курсы всех валютных пар.