---
title: Перечисление MPTHREAT_CATEGORY (Мпклиент. h)
description: Возможные категории угроз.
ms.assetid: 478ED59E-5D3C-43B3-A89D-44A649EDD086
keywords:
- MPTHREAT_CATEGORY перечисления устаревшие функции среды Windows
- PMPTHREAT_CATEGORY указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MPTHREAT_CATEGORY
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a149ef6ce6ebadacbac6f0dd35247d793ca7000
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710469"
---
# <a name="mpthreat_category-enumeration"></a>\_Перечисление категорий мпсреат

Возможные категории угроз.

## <a name="syntax"></a>Синтаксис

```C++
typedef enum tagMPTHREAT_CATEGORY {
  MP_THREAT_CATEGORY_INVALID                    = 0,
  MP_THREAT_CATEGORY_ADWARE                     = 1,
  MP_THREAT_CATEGORY_SPYWARE                    = 2,
  MP_THREAT_CATEGORY_PASSWORDSTEALER            = 3,
  MP_THREAT_CATEGORY_TROJANDOWNLOADER           = 4,
  MP_THREAT_CATEGORY_WORM                       = 5,
  MP_THREAT_CATEGORY_BACKDOOR                   = 6,
  MP_THREAT_CATEGORY_REMOTEACCESSTROJAN         = 7,
  MP_THREAT_CATEGORY_TROJAN                     = 8,
  MP_THREAT_CATEGORY_EMAILFLOODER               = 9,
  MP_THREAT_CATEGORY_KEYLOGGER                  = 10,
  MP_THREAT_CATEGORY_DIALER                     = 11,
  MP_THREAT_CATEGORY_MONITORINGSOFTWARE         = 12,
  MP_THREAT_CATEGORY_BROWSERMODIFIER            = 13,
  MP_THREAT_CATEGORY_COOKIE                     = 14,
  MP_THREAT_CATEGORY_BROWSERPLUGIN              = 15,
  MP_THREAT_CATEGORY_AOLEXPLOIT                 = 16,
  MP_THREAT_CATEGORY_NUKER                      = 17,
  MP_THREAT_CATEGORY_SECURITYDISABLER           = 18,
  MP_THREAT_CATEGORY_JOKEPROGRAM                = 19,
  MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL      = 20,
  MP_THREAT_CATEGORY_SOFTWAREBUNDLER            = 21,
  MP_THREAT_CATEGORY_STEALTHNOTIFIER            = 22,
  MP_THREAT_CATEGORY_SETTINGSMODIFIER           = 23,
  MP_THREAT_CATEGORY_TOOLBAR                    = 24,
  MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE      = 25,
  MP_THREAT_CATEGORY_TROJANFTP                  = 26,
  MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE  = 27,
  MP_THREAT_CATEGORY_ICQEXPLOIT                 = 28,
  MP_THREAT_CATEGORY_TROJANTELNET               = 29,
  MP_THREAT_CATEGORY_EXPLOIT                    = 30,
  MP_THREAT_CATEGORY_FILESHARINGPROGRAM         = 31,
  MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL      = 32,
  MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE    = 33,
  MP_THREAT_CATEGORY_TOOL                       = 34,
  MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE     = 36,
  MP_THREAT_CATEGORY_TROJAN_DROPPER             = 37,
  MP_THREAT_CATEGORY_TROJAN_MASSMAILER          = 38,
  MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE  = 39,
  MP_THREAT_CATEGORY_TROJAN_PROXYSERVER         = 40,
  MP_THREAT_CATEGORY_VIRUS                      = 42,
  MP_THREAT_CATEGORY_KNOWN                      = 43,
  MP_THREAT_CATEGORY_UNKNOWN                    = 44,
  MP_THREAT_CATEGORY_SPP                        = 45,
  MP_THREAT_CATEGORY_BEHAVIOR                   = 46,
  MP_THREAT_CATEGORY_VULNERABILTIY              = 47,
  MP_THREAT_CATEGORY_POLICY                     = 48
} MPTHREAT_CATEGORY, *PMPTHREAT_CATEGORY;
```

## <a name="constants"></a>Константы

Категория угрозы | Описание
-|-
<span id="MP_THREAT_CATEGORY_INVALID"></span><span id="mp_threat_category_invalid"></span>**Пакет управления \_ \_ \_ недопустимая категория угроз** | Категория угроз не существует или написана с ошибкой.
<span id="MP_THREAT_CATEGORY_ADWARE"></span><span id="mp_threat_category_adware"></span>**Пакет управления \_ \_ \_ рекламная программа категории угроз** | Потенциально нежелательное приложение, которое отображает рекламу.
<span id="MP_THREAT_CATEGORY_SPYWARE"></span><span id="mp_threat_category_spyware"></span>**Пакет управления \_ \_ \_ шпионское по категории угроз** | Вредоносная программа, передающая сведения об устройстве или пользователе без согласия пользователя или знания.
<span id="MP_THREAT_CATEGORY_PASSWORDSTEALER"></span><span id="mp_threat_category_passwordstealer"></span>**Пакет управления \_ \_Категория угроз \_ пассвордстеалер** | Приложение, которое собирает и (или) передает пароль злоумышленнику.
<span id="MP_THREAT_CATEGORY_TROJANDOWNLOADER"></span><span id="mp_threat_category_trojandownloader"></span>**\_Категория угроз \_ MP \_ трожандовнлоадер** | Троян, загружающий вредоносные или потенциально нежелательные приложения на зараженное устройство.
<span id="MP_THREAT_CATEGORY_WORM"></span><span id="mp_threat_category_worm"></span>**Пакет управления \_ \_ \_ червь категории угроз** | Самостоятельное распространение вредоносных программ, которые могут автоматически распространяться через сетевые подключения.
<span id="MP_THREAT_CATEGORY_BACKDOOR"></span><span id="mp_threat_category_backdoor"></span>**\_Категория угроз \_ MP \_ программы трояны** | Вредоносные программы, которые предоставляют средства обхода обычных протоколов безопасности и проверки подлинности на устройстве.
<span id="MP_THREAT_CATEGORY_REMOTEACCESSTROJAN"></span><span id="mp_threat_category_remoteaccesstrojan"></span>**Пакет управления \_ \_Категория угроз \_ ремотеакцесстрожан** | Троян, предоставляющий удаленный доступ к компьютеру.
<span id="MP_THREAT_CATEGORY_TROJAN"></span><span id="mp_threat_category_trojan"></span>**\_ \_ Троянская Категория угроз MP \_** | Вредоносное программное обеспечение, которое замаскировано как легальное программное обеспечение.
<span id="MP_THREAT_CATEGORY_EMAILFLOODER"></span><span id="mp_threat_category_emailflooder"></span>**Пакет управления \_ \_Категория угроз \_ емаилфлудер** | Вредоносная программа отправляет большой объем электронной почты на целевой объект.
<span id="MP_THREAT_CATEGORY_KEYLOGGER"></span><span id="mp_threat_category_keylogger"></span>**Пакет управления \_ \_Категория угроз \_ Троянская Keylogger** | Вредоносная программа, которая регистрирует нажатия клавиш пользователя, потенциально кража паролей и других конфиденциальных данных.
<span id="MP_THREAT_CATEGORY_DIALER"></span><span id="mp_threat_category_dialer"></span>**Пакет управления \_ \_ \_ набор "Категория угроз** " | Вредоносные программы, которые делают неавторизованные телефонные звонки, часто на тарифы уровня "Премиум".
<span id="MP_THREAT_CATEGORY_MONITORINGSOFTWARE"></span><span id="mp_threat_category_monitoringsoftware"></span>**Пакет управления \_ \_Категория угроз \_ мониторингсофтваре** | Потенциально нежелательное приложение, отслеживающее активность пользователей, например, тип пользователя на клавиатуре или представления на экране.
<span id="MP_THREAT_CATEGORY_BROWSERMODIFIER"></span><span id="mp_threat_category_browsermodifier"></span>**Пакет управления \_ \_Категория угроз \_ бровсермодифиер** | Потенциально нежелательное приложение, которое изменяет параметры веб-браузера без согласия пользователя.
<span id="MP_THREAT_CATEGORY_COOKIE"></span><span id="mp_threat_category_cookie"></span>**Пакет управления \_ \_ \_ файл cookie категории угроз** | Данные, которые веб-сервер отправляет браузеру, позволяя сохранять сведения о пользователе, такие как параметры веб-приложения, на повторяющихся посещениях.
<span id="MP_THREAT_CATEGORY_BROWSERPLUGIN"></span><span id="mp_threat_category_browserplugin"></span>**Пакет управления \_ \_Категория угроз \_ бровсерплугин** | Программное обеспечение, позволяющее стандартному веб-браузеру отображать и запускать определенные типы содержимого, такие как файлы мультимедиа, анимированные изображения и интерактивные формы.
<span id="MP_THREAT_CATEGORY_AOLEXPLOIT"></span><span id="mp_threat_category_aolexploit"></span>**Пакет управления \_ \_Категория угроз \_ аолексплоит** | Вредоносные программы, которые атакуют пользователей Интернет службы AOL, часто извлекая пароли или изменяя параметры.
<span id="MP_THREAT_CATEGORY_NUKER"></span><span id="mp_threat_category_nuker"></span>**Пакет управления \_ \_ \_ Удалить категорию угроз** | Вредоносная программа, предназначенная для аварийного завершения работы устройства или уменьшения ее стабильности.
<span id="MP_THREAT_CATEGORY_SECURITYDISABLER"></span><span id="mp_threat_category_securitydisabler"></span>**Пакет управления \_ \_Категория угроз \_ секуритидисаблер** | Вредоносная программа, которая отключает параметры безопасности или продукты.
<span id="MP_THREAT_CATEGORY_JOKEPROGRAM"></span><span id="mp_threat_category_jokeprogram"></span>**Пакет управления \_ \_Категория угроз \_ жокепрограм** | Приложение, предназначенное для амусе или пугают пользователя без фактического ущерба для устройства.
<span id="MP_THREAT_CATEGORY_HOSTILEACTIVEXCONTROL"></span><span id="mp_threat_category_hostileactivexcontrol"></span>**Пакет управления \_ \_Категория угроз \_ хостилеактивексконтрол** | Элемент управления ActiveX, разработанный злоумышленником для причинения вреда устройству. Элемент управления ActiveX — это разновидность надстройки браузера Internet Explorer.
<span id="MP_THREAT_CATEGORY_SOFTWAREBUNDLER"></span><span id="mp_threat_category_softwarebundler"></span>**Пакет управления \_ \_Категория угроз \_ софтваребундлер** | Программное обеспечение, устанавливающее другие потенциально нежелательные приложения, например рекламное по или шпионское по. Для работы с лицензионным соглашением по объединению программного обеспечения могут потребоваться другие компоненты.
<span id="MP_THREAT_CATEGORY_STEALTHNOTIFIER"></span><span id="mp_threat_category_stealthnotifier"></span>**Пакет управления \_ \_Категория угроз \_ стеалснотифиер** | Вредоносная программа, которая подключается к удаленному серверу через скрытое подключение для уведомления злоумышленника об установке вредоносной программы.
<span id="MP_THREAT_CATEGORY_SETTINGSMODIFIER"></span><span id="mp_threat_category_settingsmodifier"></span>**Пакет управления \_ \_Категория угроз \_ сеттингсмодифиер** | Потенциально нежелательное приложение, которое изменяет параметры пользователя без ведома или согласия пользователя.
<span id="MP_THREAT_CATEGORY_TOOLBAR"></span><span id="mp_threat_category_toolbar"></span>**Пакет управления \_ \_ \_ панель инструментов категории угроз** | Потенциально нежелательное приложение (PUA), которое устанавливает панель инструментов в веб-браузере пользователя; часто входит в состав дополнительных PUA, таких как рекламное по.
<span id="MP_THREAT_CATEGORY_REMOTECONTROLSOFTWARE"></span><span id="mp_threat_category_remotecontrolsoftware"></span>**Пакет управления \_ \_Категория угроз \_ ремотеконтролсофтваре** | Потенциально нежелательное приложение, предоставляющее удаленный доступ к устройству.
<span id="MP_THREAT_CATEGORY_TROJANFTP"></span><span id="mp_threat_category_trojanftp"></span>**Пакет управления \_ \_Категория угроз \_ трожанфтп** | Троян, использующий FTP-сервер, чтобы позволить злоумышленнику отправлять или скачивать файлы с устройства.
<span id="MP_THREAT_CATEGORY_POTENTIALUNWANTEDSOFTWARE"></span><span id="mp_threat_category_potentialunwantedsoftware"></span>**Пакет управления \_ \_Категория угроз \_ потентиалунвантедсофтваре** | Также известно как *потенциально нежелательное приложение* или *PUA*; программное обеспечение, которое может работать с чрезмерным вмешательством, которое пользователь может не получить или полностью передать.
<span id="MP_THREAT_CATEGORY_ICQEXPLOIT"></span><span id="mp_threat_category_icqexploit"></span>**Пакет управления \_ \_Категория угроз \_ иккексплоит** | Троян, который подключается к службе обмена сообщениями ICQ-, часто путем извлечения паролей или изменения параметров.
<span id="MP_THREAT_CATEGORY_TROJANTELNET"></span><span id="mp_threat_category_trojantelnet"></span>**Пакет управления \_ \_Категория угроз \_ трожантелнет** | Троян, устанавливающий сервер Telnet на компьютере пользователя без ведома или согласия пользователя.
<span id="MP_THREAT_CATEGORY_EXPLOIT"></span><span id="mp_threat_category_exploit"></span>**Пакет управления \_ \_ \_ ЭКСПЛОЙТ категории угроз** | Вредоносный код, использующий преимущества уязвимости устройства или системы.
<span id="MP_THREAT_CATEGORY_FILESHARINGPROGRAM"></span><span id="mp_threat_category_filesharingprogram"></span>**Пакет управления \_ \_Категория угроз \_ филешарингпрограм** | Потенциально нежелательное приложение, которое открывает устройство для совместного использования файлов на одноранговом устройстве.
<span id="MP_THREAT_CATEGORY_MALWARE_CREATION_TOOL"></span><span id="mp_threat_category_malware_creation_tool"></span>**Пакет управления \_ \_Категория угроз \_ \_ \_ средство создания вредоносных программ** | Приложение, которое может автоматически создавать вредоносные файлы.
<span id="MP_THREAT_CATEGORY_REMOTE_CONTROL_SOFTWARE"></span><span id="mp_threat_category_remote_control_software"></span>**Пакет управления \_ \_ \_ \_ \_ программное обеспечение удаленного управления категории угроз** | Потенциально нежелательное приложение, которое обеспечивает удаленный доступ к устройству.
<span id="MP_THREAT_CATEGORY_TOOL"></span><span id="mp_threat_category_tool"></span>**Пакет управления \_ \_ \_ средство категории угроз** | Служебная программа, которая помогает злоумышленникам выполнять вредоносные действия на устройстве.
<span id="MP_THREAT_CATEGORY_TROJAN_DENIALOFSERVICE"></span><span id="mp_threat_category_trojan_denialofservice"></span>**Пакет управления \_ \_Категория угроз \_ Троян \_ дениалофсервице** | Троян, предназначенный для отправки большого объема сетевых запросов к целевой службе в рамках атаки типа "отказ в обслуживании" (DoS).
<span id="MP_THREAT_CATEGORY_TROJAN_DROPPER"></span><span id="mp_threat_category_trojan_dropper"></span>**Пакет управления \_ \_Категория угроз \_ Троян \_ -сбрасыватель** | Троян, который скачивает и устанавливает вредоносные и потенциально нежелательные приложения на целевом объекте.
<span id="MP_THREAT_CATEGORY_TROJAN_MASSMAILER"></span><span id="mp_threat_category_trojan_massmailer"></span>**Пакет управления \_ \_Категория угроз \_ Троян \_ массмаилер** | Троян, отправляющий большой объем электронной почты на целевой объект, предназначенный для перегрузки папки "Входящие" целевого объекта.
<span id="MP_THREAT_CATEGORY_TROJAN_MONITORINGSOFTWARE"></span><span id="mp_threat_category_trojan_monitoringsoftware"></span>**Пакет управления \_ \_Категория угроз \_ Троян \_ мониторингсофтваре** | Троян, отслеживающий активность пользователей, например, тип пользователя на клавиатуре или представления на экране.
<span id="MP_THREAT_CATEGORY_TROJAN_PROXYSERVER"></span><span id="mp_threat_category_trojan_proxyserver"></span>**Пакет управления \_ \_Категория угроз \_ Троян \_ PROXYSERVER** | Прокси-сервер, установленный трояном, предоставляя непрерывное подключение к Интернету и разрешающее несанкционированный доступ к зараженному устройству.
<span id="MP_THREAT_CATEGORY_VIRUS"></span><span id="mp_threat_category_virus"></span>**Пакет управления \_ \_ \_ вирус категории угроз** | Вредоносные программы, которые реплицируют, как правило, заражая другие файлы в системе, тем самым позволяя выполнять код вредоносных программ и его распространение при активации этих файлов.
<span id="MP_THREAT_CATEGORY_KNOWN"></span><span id="mp_threat_category_known"></span>**Пакет управления \_ \_ \_ известная категория угроз** | Неопределенная угроза вредоносных программ.
<span id="MP_THREAT_CATEGORY_UNKNOWN"></span><span id="mp_threat_category_unknown"></span>**Пакет управления \_ \_Категория угрозы \_ неизвестна** | Неуказанная вредоносная программа, которая еще не была определена.
<span id="MP_THREAT_CATEGORY_SPP"></span><span id="mp_threat_category_spp"></span>**Пакет управления \_ \_Категория угроз \_ SPP** | Технология борьбы с пиратством, которая требует, чтобы каждая установка продукта Windows была активирована корпорацией Майкрософт.
<span id="MP_THREAT_CATEGORY_BEHAVIOR"></span><span id="mp_threat_category_behavior"></span>**Пакет управления \_ \_ \_ поведение категории угроз** | Тип обнаружения на основе действий с файлами, которые часто связаны с вредоносными действиями.
<span id="MP_THREAT_CATEGORY_VULNERABILTIY"></span><span id="mp_threat_category_vulnerabiltiy"></span>**Пакет управления \_ \_Категория угроз \_ вулнерабилтий** | Любой недостаток, административный процесс или действие, которые делают устройство уязвимым для использования угрозой.
<span id="MP_THREAT_CATEGORY_POLICY"></span><span id="mp_threat_category_policy"></span>**Пакет управления \_ \_ \_ Политика категории угроз** | Набор правил, определяемых администратором и управляющих функциями настольных и мобильных устройств, таких как обновления программного обеспечения.

## <a name="requirements"></a>Требования

| Требование | Значение |
|-|-|
| Минимальная версия клиента | Windows 8 (только для классических приложений) |
| Минимальная версия сервера | Windows Server 2012 (только для классических приложений) |
| Header | Мпклиент. h |
