# Руководство по сохранению связи

## Приложения для установки

Если связь с магазинами приложений не закрыта, скачайте и установите
следующие приложения

- ExpressVPN - платный VPN клиент:
  [iOS](https://apps.apple.com/ru/app/expressvpn-c%D0%B0%D0%BC%D0%B0%D1%8F-%D0%BD%D0%B0%D0%B4%D0%B5%D0%B6%D0%BD%D0%B0%D1%8F-vpn/id886492891), [Android](https://play.google.com/store/apps/details?id=com.expressvpn.vpn&hl=ru&gl=US), [Windows/MacOS/Linux](https://www.expressvpn.com/ru/vpn-software)
- Telegram - мессенджер: [iOS](https://apps.apple.com/ru/app/telegram/id686449807),
  [Android](https://play.google.com/store/apps/details?id=org.telegram.messenger&hl=ru&gl=US), [Windows/MacOS/Linux](https://desktop.telegram.org/)
- WireGuard - Peer-to-Peer VPN клиент: [iOS](https://apps.apple.com/ru/app/wireguard/id1441195209), 
  [Android](https://play.google.com/store/apps/details?id=com.wireguard.android&hl=ru&gl=US), [Windows/MacOS/Linux](https://www.wireguard.com/install/)
- Signal - приватный мессенджер:
  [iOS](https://apps.apple.com/ru/app/signal-%D0%BF%D1%80%D0%B8%D0%B2%D0%B0%D1%82%D0%BD%D1%8B%D0%B9-%D0%BC%D0%B5%D1%81%D1%81%D0%B5%D0%BD%D0%B4%D0%B6%D0%B5%D1%80/id874139669), [Android](https://play.google.com/store/apps/details?id=org.thoughtcrime.securesms&hl=ru&gl=US), [Windows/MacOS/Linux](https://signal.org/ru/download/)
- Element - безопасный групповой чат на основе протокола Matrix:
  [iOS](https://apps.apple.com/ru/app/element-messenger/id1083446067),
  [Android](https://play.google.com/store/apps/details?id=im.vector.app&hl=ru&gl=US), [Windows/MacOS/Linux](https://element.io/get-started#download)

## Конфигурация VPN

VPN - Virtual Private Network - виртуальная частная сеть - способ подключения
к сети, когда устройство (телефон или компьютер) вместо соединения с разными
сайтами и серверами напрямую, выполяняет подсоединение через посредника (его
называют "прокси-сервером" или "мостом"). Есть несколько разных типов VPN и они
отличаются способами работы. В iOS (айфоны и айпады) уже встроено 3 типа VPN:
IKEv2, IPSEC и L2TP. На iOS также можно установить другие типы VPN. Платные
провайдеры VPN выкладывают в App Store свои приложения. Одно из них -
ExpressVPN - в списке выше. Еще один тип - WireGuard - протокол с открытым
кодом. 

За доступ через проприетарный VPN типа ExpressVPN, Mullvad, NordVPN итд - нужно
платить соответствующей компании помесячно или раз в год. Эти компании
обслуживают свои собственные прокси-сервера. IPSEC, IKEv2, L2TP, WireGuard -
открытые протоколы и люди, знакомые с системным администрированием могут
запустить прокси-серверы на хостинг-компании за границей.

### Настройка IKEv2 на iOS

Если кто-то создал для вас IKEv2 VPN сервер, нужно сделать следующие шаги на
iOS устройстве (указываются названия в русском и английском интерфейсах).

Вы получите послание через один из доступных каналов со следующей
информацией:

- Файл серверного сертификата (обычно с расширением .pem)
- Адрес сервера
- Имя пользователя
- Пароль

1. Откройте в почте или мессенджере файл сертификата. Файл откроется и
   установится на устройство, но его нужно будет активировать в настройках.
   Перейдите в приложение "Настройки" (Settings) и под именем пользователя 
   будет кнопка "Профиль загружен". Нажмите на нее и в диалоге нажмите "Установить"
   ("Install") и введите ваш пин-код и подтверждате, пока сертификат не будет
   установлен. Игнорируйте красную надпись "Не проверен" ("not verified"). 
2. Откройте приложение Настройки (Settings), Основные (General), "VPN и
   управление устройством" ("VPN & Device Management").
   Зайдите в секцию VPN и нажмите кнопку "Добавить конфигурацию VPN..." ("Add
   VPN Configuration...").
3. В разделе "Тип" ("Type") выберите IKEv2. Заполните "Описание" 
   ("Description")любым именем, но 
   не используйте никакой идентифицирующей информации (не пишите "Vanin VPN", 
   а лучше "Мост через реку" или что-то подобное).
4. Во ввод "Сервер" ("Server") впишите полученный адрес сервера. В строку 
   "Удаленный ID" ("Remote ID") впишите адрес сервера еще разю
5. Оставьте "Локальный ID" ("Local ID") пустым
6. В параметрах аутентификации выберите для "Аутентификация" ("User
   Authentication") значение "Имя
   пользователя" ("Username"). В графах "Имя пользователя" ("Username") и 
   "Пароль" ("Password") впишите полученные имя
   пользователя и пароль.
7. Нажмите "Готово" ("Done").

Для активизации VPN выберите подклчение в списке (если у вас их несколько) и
переведите переключатель "Статус" ("Status") из положения "Не подключено" 
("Not Connected") в положение "Подключено" ("Connected"). VPN выключается в
обратном порядке. 


## Полезные ссылки

### Технические руководства

- [OpenRunet - РосКомСвобода](https://openrunet.org/)




