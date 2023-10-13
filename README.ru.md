README: [🇺🇸](/README.md) | [🇷🇺](/README.ru.md)

# ITL_noafk

Простой серверный плагин для BeamMP. Плагин позволяет кикать AFK игроков и удалять брошенные машины.

## Установка и обновление

- Скачайте архив и просто перенесите папку "ITL_noafk" в директорию "Resources/Server" вашего сервера

## Конфигурирование

Объяснение строчек конфига:
```
"vehiclePositionsCheckDelay": 5,                            // Проверка раз в N секунд
"kickAfkPlayers": true,                                     // Кикать игроков за АФК  (игрок должен быть с транспортом!, если у игрока несколько машин то должны стоять все!)
"kickAfkPlayersChecksCount": 60,                            // Кол-во проверок через которое АФК игрока кикнет
"kickAfkPlayersNotifyPlayer": true,                         // Уведомлять игрока что его кикнет за АФК (true - да, false - нет)
"kickAfkPlayersNotifyPlayerAfterCount": 50,                 // Кол-во проверок через которое игрока будет уведомлять что он долго АФК и что его кикнет
"kickAfkPlayersWoVehicles": true,                           // Кикать АФК игроков без транскорта (true - да, false - нет)
"kickAfkPlayersWoVehiclesChecksCount": 120,                 // Кол-во проверок через которое АФК игрока без транспорта кикнет
"kickAfkPlayersWoVehiclesNotifyPlayer": true,               // Уведомлять АФК игрока без транспорта что его кикнет (true - да, false - нет)
"kickAfkPlayersWoVehiclesNotifyPlayerAfterCount": 110,      // Кол-во проверок через которое АФК игрока без транспорта будет уведомлять
"destroyAbandonedVehicle": true,                            // Удалять неиспользуемый транспорт (true - да, false - нет)
"destroyAbandonedVehicleChecksCount": 120,                  // Кол-во проверок через которое удалится неиспользуемый транспорт
"destroyAbandonedVehicleNotifyPlayer": true,                // Уведомлять игрока что его неиспользуемый транспорт удалится (true - да, false - нет)
"destroyAbandonedVehicleNotifyPlayerAfterCount": 110,       // Кол-во проверок через которое игрока будет уведомлять что его неиспользуемый транспорт удалится
"debug": false                                              // Режим отладки (true - включить, false - выключить | рекомендуется false)
```

## Рекомендации

Если "destroyAbandonedVehicle": true и "kickAfkPlayers": true то рекомендуется сделать количество проверок через которое удалится неиспользуемый транспорт больше чем количество проверок через которое АФК игрока кикнет или включить "kickAfkPlayersWoVehicles": true иначе у АФК игрока удалится транспорт и плагин не сможет его кикнуть.

Рекомендуется ставить "kickAfkPlayersNotifyPlayerAfterCount": 50, меньше чем "kickAfkPlayersChecksCount": 60,(и подобные параметры) иначе игрока не будет уведомлять.

Если вам нужно узнать время через которое игрока кикнет надо "vehiclePositionsCheckDelay": 5, умножить на "kickAfkPlayersChecksCount": 60,(или подобные параметры) в данном примере игрока кикнет через 300 секунд (5 минут)

## Благодарности

[csv4211](https://github.com/csv4211) и [STRMBRG](https://github.com/STRMBRG) за помощь с документацией и тестированием
