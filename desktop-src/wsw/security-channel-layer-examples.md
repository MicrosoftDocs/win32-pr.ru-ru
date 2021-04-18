---
title: Примеры уровней каналов безопасности
description: В следующих примерах демонстрируется безопасность на уровне канала.
ms.assetid: ac4f0275-4783-411d-98da-2c5a1a169dcc
keywords:
- Примеры безопасности
- Примеры безопасности, Настройка
- ввсапи
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b1283339b1a4af624e118e3f6c76a07449f9274
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700619"
---
# <a name="security-channel-layer-examples"></a>Примеры уровней каналов безопасности

В следующих примерах демонстрируется безопасность на [уровне канала](channel-layer-overview.md) .

Безопасность транспорта Windows через TCP: Клиент: [рекуестреплиткпклиентвисвиндовстранспортсекуритексампле](requestreplytcpclientwithwindowstransportsecurityexample.md), сервер: [рекуестреплиткпсервервисвиндовстранспортсекуритексампле](requestreplytcpserverwithwindowstransportsecurityexample.md).

Безопасность транспорта Windows через именованные каналы: Клиент: [рекуестреплинамедпипесклиентвисвиндовстранспортсекуритексампле](requestreplynamedpipesclientwithwindowstransportsecurityexample.md), сервер: [рекуестреплинамедпипессервервисвиндовстранспортсекуритексампле](requestreplynamedpipesserverwithwindowstransportsecurityexample.md).

Безопасность транспорта SSL: Клиент: [хттпклиентвиссслексампле](httpclientwithsslexample.md), сервер: [хттпсервервиссслексампле](httpserverwithsslexample.md).

Имя пользователя для смешанного режима безопасности SSL: Клиент: [хттпклиентвисусернамеоверсслексампле](httpclientwithusernameoversslexample.md), сервер: [хттпсервервисусернамеоверсслексампле](httpserverwithusernameoversslexample.md).

Имя пользователя для смешанного режима безопасности SSL: Клиент: [хттпклиентвискерберосоверсслексампле](httpclientwithkerberosoversslexample.md), сервер: [хттпсервервискерберосоверсслексампле](httpserverwithkerberosoversslexample.md).

Имя пользователя в смешанном режиме безопасности SSL: [метадатаимпортвисусернамеоверсслексампле](metadataimportwithusernameoversslexample.md). Выданный маркер по безопасности смешанного режима SSL: [метадатаимпортвисиссуедтокеноверсслексампле](metadataimportwithissuedtokenoversslexample.md). Сертификат X509 в смешанном режиме безопасности SSL: [MetadataImportWithX509OverSslExample](metadataimportwithx509oversslexample.md).

## <a name="one-time-setup-for-security-samples"></a>One-Time установки для примеров безопасности

Для запуска примеров безопасности ВВСАПИ необходимо настроить сертификаты клиента и сервера для SSL, а также локальную учетную запись пользователя для проверки подлинности заголовка HTTP. Перед началом работы необходимы следующие средства:

-   MakeCert.exe (доступно в пакете SDK для Windows 7.)
-   CertUtil.exe или CertMgr.exe (CertUtil.exe доступен в Windows SDK, начиная с Windows Server 2003. CertMgr.exe доступен в пакете SDK для Windows 7. Вам нужен только один из этих средств.)
-   HttpCfg.exe: (это необходимо, только если вы используете Windows 2003 или Windows XP. Это средство доступно в средствах поддержки Windows XP SP2, а также на компакт-диске Windows Server 2003 Resource Kit Tools.)

Если вы получаете примеры ВВСАПИ, установив пакет SDK для Windows 7, можно найти MakeCert.exe и CertMgr.exe в разделе% ProgramFiles% \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ bin.

Выполните следующие пять шагов установки из командной строки (с повышенными правами при использовании Windows Vista и более поздних версий):

1.  Создайте самозаверяющий сертификат в качестве центра сертификации (ЦС) или издателя: **MakeCert.exe-SS root-SR-n "CN = имитировать-Test-Калифорния"-CY Authority-r-SK "какэйконтаинер"**
2.  Создайте сертификат сервера, используя предыдущий сертификат в качестве издателя: **MakeCert.exe-SS My-SR LocalMachine-n "CN = localhost"-Небесный Exchange-является корневым-IR хранилище LocalMachine-in-тест-CA-SK "серверкэйконтаинер"**
3.  Найдите отпечаток (40-символьный хэш SHA-1) сертификата сервера, выполнив одну из приведенных ниже команд и выполнив поиск сертификата с именем localhost с помощью команды Issuer-тест-CA:
    -   **CertUtil.exe — сохранить мое localhost**
    -   **CertMgr.exe-s-r LocalMachine My**
4.  Зарегистрируйте сертификат сервера? s отпечаток без пробелов с HTTP.SYS:
    -   В Windows Vista и более поздних версиях (параметр AppID является произвольным GUID): **Netsh.exe http add sslcert иппорт = 0.0.0.0:8443 AppID = {00112233-4455-6677-8899-AABBCCDDEEFF}** certhash =<40CharacterThumbprint>
    -   В Windows XP или 2003: **HttpCfg.exe Set SSL-i 0.0.0.0:8443-h <40CharacterThumbprint>**
5.  Создание локального пользователя: **net user "тестусерфорбасикаус" "TstPWD@ \* 4Bsic"/Add**

Чтобы очистить сертификаты, привязку SSL-сертификата и учетную запись пользователя, созданную на предыдущих шагах, выполните следующие команды. Обратите внимание, что при наличии нескольких сертификатов с одинаковыми именами CertMgr.exe потребуется ввести их перед их удалением.

-   **CertMgr.exe-del-c-n поддельный-Test-CA-s-корневой узел LocalMachine**
-   **CertMgr.exe-del-c-n localhost-s-r LocalMachine My**
-   **Netsh.exe HTTP DELETE sslcert иппорт = 0.0.0.0:8443 (или HttpCfg.exe удалить SSL-i 0.0.0.0:8443)**
-   **NET User "Тестусерфорбасикаус"/Delete**

Убедитесь, что существует только один корневой сертификат с именем "фальшивый — тест-CA". Если вы не уверены, в этом случае всегда можно попробовать очистить эти сертификаты с помощью приведенных выше команд очистки (и пропускать ошибки) перед запуском 5-шаговой установки.

 

 




