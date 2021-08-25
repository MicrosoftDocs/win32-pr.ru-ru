---
description: Демонстрирует использование основных функций управления беспроводной сетью.
ms.assetid: 63af0b88-c20b-4b06-9db3-e8510fc80053
title: Пример собственного API WiFi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ed28fadcd73eb4b3e632702078280ddba55d683c66decfdf03bc948182c52d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801064"
---
# <a name="native-wifi-api-sample"></a>Пример собственного API WiFi

встроенный пример API Wifi, демонстрирующий использование основных функций управления беспроводной сетью, входит в состав пакета средств разработки Microsoft Windows Software Development Kit (SDK). последняя версия Windows SDK доступна в [центре загрузки](https://developer.microsoft.com/windows/downloads).

По умолчанию исходный код образца Wi-Fi устанавливается в следующем каталоге:

**C: \\ Program files \\ Microsoft sdks \\ Windows \\ <version number> \\ примеры \\ нетдс \\ Wlan**

Собственный пример API WiFi находится в следующей папке:

**AutoConfig**

встроенный пример wi-fi можно скомпилировать и запустить в Windows Vista и более поздних версий, Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2). некоторые функции примера не поддерживаются в Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2). список функций, поддерживаемых Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2), см. [в статье поддержка api wi-fi в Windows XP](about-wireless-lan-api-for-windows-xp-service-pack-2.md)

В примере машинного кода WiFi показано, как выполнять следующие задачи.

-   Перечисление беспроводных интерфейсов. См. [**вланенуминтерфацес**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces).
-   Получите возможности интерфейса. См. [**вланжетинтерфацекапабилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetinterfacecapability).

    * * Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2): * * эта функция не поддерживается.

-   Запрос интерфейса. См. [**вланкуеринтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface).
-   Задайте параметры для сетевого интерфейса. См. [**влансетинтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface). Эта функция может использоваться для включения и отключения беспроводного радио (и, следовательно, включения или отключения беспроводных сетевых подключений).
-   Проверьте наличие доступных беспроводных сетей. См. [**вланскан**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan).
-   Получение списка доступных или видимых беспроводных сетей. См. [**вланжетаваилабленетворклист**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist).
-   Получение, сохранение или удаление профиля. См. раздел [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile), [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)и [**вланделетепрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile).
-   Подключение или отключение от беспроводной сети. См. раздел [**вланконнект**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect) and [**вландисконнект**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование собственного WiFi](using-native-wifi.md)
</dt> <dt>

[Windows Форум по пакету SDK для беспроводной сети Vista](https://social.msdn.microsoft.com/Forums/b6bbd8f0-a921-480f-9b4b-845336462bc0/welcome-to-the-windows-vista-wireless-sdk-forum)
</dt> <dt>

[устранение неполадок беспроводных подключений Windows Vista 802,11](/previous-versions/windows/it-pro/windows-vista/cc766215(v=ws.10))
</dt> </dl>

 

 
