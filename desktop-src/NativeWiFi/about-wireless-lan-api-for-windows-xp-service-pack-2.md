---
description: подмножество встроенных функций интерфейса API Wifi поддерживается в Windows XP с пакетом обновления 2 (sp2) и Windows XP с пакетом обновления 3 (sp3).
ms.assetid: d32c4a03-59e8-4fdd-9d5a-e7ef0eb25e84
title: встроенная поддержка интерфейса API Wifi в Windows XP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc284ed24a6aa6ddb266b410a6233c15e063bf909aa9c82f0afa3dc070c9289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685314"
---
# <a name="native-wifi-api-support-on-windows-xp"></a>встроенная поддержка интерфейса API Wifi в Windows XP

подмножество встроенных функций интерфейса API Wifi поддерживается в Windows XP с пакетом обновления 2 (sp2) и Windows XP с пакетом обновления 3 (sp3). эта функция включена в Windows XP с пакетом обновления 3 (SP3) по умолчанию. в Windows XP с пакетом обновления 2 (sp2) эту функцию можно добавить, применив исправление, которое называется API беспроводной локальной сети для Windows XP с пакетом обновления 2 (sp2). дополнительные сведения или о загрузке исправления см. в разделе "разработчики не могут создавать беспроводные клиентские программы, управляющие профилями и подключениями по беспроводной службе настройки в Microsoft Windows XP с пакетом обновления 2 (SP2)" в центре знаний справки и поддержки по адресу [https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997) .

из-за базовых архитектурных различий в Windows XP встроенный API wi-fi в имеет некоторые ограничения. Ниже приведен список ограничений.

-   С профилем можно связать не более одного SSID.
-   Сети инфраструктуры всегда отображаются перед сетями ad hoc в списке профилей.
-   Имена профилей являются производными от SSID и не могут быть заданы пользователем произвольной строкой.
-   Типы PHY не поддерживаются.
-   Кэширование парных главных ключей (PMK) не поддерживается.
-   Функции расширяемости независимых поставщиков оборудования (IHV) не поддерживаются.
-   Разрешения профиля не поддерживаются.
-   \_ \_ Доступны только подключение к ACM по беспроводной сети \_ \_ и уведомления \_ о \_ разъединении ACM для уведомлений WLAN \_ .
-   Глобальные параметры конфигурации 802.1 X и EAPOL не поддерживаются.

Windows XP с пакетом обновления 3 (SP3) и API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2) поддерживают следующие функции:

-   [**\_ \_ обратный вызов уведомления WLAN**](/windows/win32/api/wlanapi/nc-wlanapi-wlan_notification_callback)
-   [**вланаллокатемемори**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanallocatememory)
-   [**вланклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanclosehandle)
-   [**вланконнект**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanconnect)
-   [**вланделетепрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandeleteprofile)
-   [**вландисконнект**](/windows/desktop/api/wlanapi/nf-wlanapi-wlandisconnect)
-   [**вланенуминтерфацес**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanenuminterfaces)
-   [**вланфримемори**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanfreememory)
-   [**вланжетаваилабленетворклист**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetavailablenetworklist)
-   [**вланжетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile)
-   [**вланжетпрофилелист**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofilelist)
-   [**вланопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanopenhandle)
-   [**вланкуеринтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface)
-   [**вланреасонкодетостринг**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanreasoncodetostring)
-   [**вланрегистернотификатион**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanregisternotification)
-   [**вланскан**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
-   [**влансетинтерфаце**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlansetinterface)
-   [**влансетпрофиле**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile)
-   [**влансетпрофилиапксмлусердата**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileeapxmluserdata)
-   [**влансетпрофилелист**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofilelist)
-   [**влансетпрофилепоситион**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofileposition)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[https://support.microsoft.com/kb/918997](https://support.microsoft.com/kb/918997)
</dt> <dt>

[О встроенных WiFi](about-native-wifi.md)
</dt> </dl>

 

 
