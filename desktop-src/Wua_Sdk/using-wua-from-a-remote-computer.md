---
description: API Центр обновления Windows Agent (WUA) может использоваться пользователем на удаленном компьютере или приложением, которое работает на удаленном компьютере. Однако у удаленного пользователя или приложения должны быть права администратора.
ms.assetid: 15f86590-bed8-4506-916d-43b0bac5db2a
title: Использование агента WUA с удаленного компьютера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0a3780099f6ff9707893c9f7b5d5f2f18be1f6a97c33d9133fef4d5d3497087
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737783"
---
# <a name="using-wua-from-a-remote-computer"></a>Использование агента WUA с удаленного компьютера

API Центр обновления Windows Agent (WUA) может использоваться пользователем на удаленном компьютере или приложением, которое работает на удаленном компьютере. Однако у удаленного пользователя или приложения должны быть права администратора.

В следующем списке содержатся интерфейсы, доступные для удаленных пользователей и приложений.

-   [**иупдатесессион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession)
-   [**IUpdateSession2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesession2)
-   [**иупдатесеарчер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatesearcher)
-   [**иаутоматикупдатес**](/windows/desktop/api/Wuapi/nn-wuapi-iautomaticupdates)
-   [**исеарчресулт**](/windows/desktop/api/Wuapi/nn-wuapi-isearchresult)
-   [**иупдатеколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatecollection)
-   [**иупдате**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate)
-   [**IUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdate2)
-   [**ивиндовсдриверупдате**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate)
-   [**IWindowsDriverUpdate2**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsdriverupdate2)
-   [**иупдатеидентити**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateidentity)
-   [**иимажеинформатион**](/windows/desktop/api/Wuapi/nn-wuapi-iimageinformation)
-   [**иинсталлатионбехавиор**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior)
-   [**истрингколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-istringcollection)
-   [**иупдатехисторентриколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentrycollection)
-   [**иупдатехисторентри**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatehistoryentry)
-   [**икатегориколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-icategorycollection)
-   [**икатегори**](/windows/desktop/api/Wuapi/nn-wuapi-icategory)
-   [**иупдатиксцептионколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexceptioncollection)
-   [**иупдатиксцептион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateexception)
-   [**иупдатедовнлоадконтентколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontentcollection)
-   [**иупдатедовнлоадконтент**](/windows/desktop/api/Wuapi/nn-wuapi-iupdatedownloadcontent)
-   [**иупдатесервицеманажер**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager)
-   [**иупдатесервицеколлектион**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicecollection)
-   [**иупдатесервице**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice)
-   [**ивиндовсупдатеажентинфо**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo)

В следующем списке содержатся интерфейсы и свойства, недоступные для удаленных пользователей и приложений.

-   [**Иупдатесессион:: Креатеупдатедовнлоадер**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdatedownloader)
-   [**Иупдатесессион:: Креатеупдатеинсталлер**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-createupdateinstaller)
-   [**Свойство WebProxy объекта Иупдатесессион**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesession-get_webproxy)
-   [**Иупдатесеарчер:: Бегинсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-beginsearch)
-   [**Иупдатесеарчер:: Ендсеарч**](/windows/desktop/api/Wuapi/nf-wuapi-iupdatesearcher-endsearch)
-   [**Свойство иупдате**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-get_ishidden) (**Hidden** доступно только для чтения, если оно вызывается удаленно.)
-   [**Иупдате:: AcceptEula**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-accepteula)
-   [**Иупдате:: Копифромкаче**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate-copyfromcache)
-   [**IUpdate2:: Копитокаче**](/windows/desktop/api/Wuapi/nf-wuapi-iupdate2-copytocache)
-   [**IWindowsDriverUpdate2:: Копитокаче**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsdriverupdate2-copytocache)
-   [**Иупдатесервицеманажер:: AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)
-   [**Иупдатесервицеманажер:: Регистерсервицевисау**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)
-   [**Иупдатесервицеманажер:: Унрегистерсервицевисау**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau)
-   [**Иаутоматикупдате::P Аусе**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-pause)
-   [**Иаутоматикупдатес:: Resume**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-resume)
-   [**Иаутоматикупдатес:: Шовсеттингсдиалог**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-showsettingsdialog)
-   [**Параметры Свойство объекта Иаутоматикупдатес**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_settings)
-   [**Свойство Сервицеенаблед объекта Иаутоматикупдатес**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-get_serviceenabled)
-   [**Иаутоматикупдатес:: Енаблесервице**](/windows/desktop/api/Wuapi/nf-wuapi-iautomaticupdates-enableservice)
-   [**исистеминформатион**](/windows/desktop/api/Wuapi/nn-wuapi-isysteminformation)

следующие порты и исключения необходимо добавить в Windows параметры брандмауэра для Windows Vista и Windows Server 2008 для удаленного вызова API WUA.

<dl> <dt>

<span id="Exception_1"></span><span id="exception_1"></span><span id="EXCEPTION_1"></span>Исключение 1
</dt> <dd> <dl> <dd>Локальный порт: 135</dd> <dd>Удаленный порт: все</dd> <dd>Номер протокола: 6</dd> <dd>Исполняемый файл:% WINDIR% \\ system32 \\svchost.exe</dd> <dd>Служба: RPCSS</dd> <dd>Удаленное право: администратор</dd> </dl> </dd> <dt>

<span id="Exception_2"></span><span id="exception_2"></span><span id="EXCEPTION_2"></span>Исключение 2
</dt> <dd> <dl> <dd>Локальный порт: динамический RPC</dd> <dd>Удаленный порт: все</dd> <dd>Номер протокола: 6</dd> <dd>Исполняемый файл:% WINDIR% \\ system32 \\dllhost.exe</dd> <dd>Удаленное право: администратор</dd> </dl> </dd> </dl>

в следующем списке содержатся средства, которые можно использовать для настройки параметров брандмауэра Windows.

-   Брандмауэр Windows с оснасткой «Повышенная безопасность».
-   Групповая политика
-   Программа командной строки netsh advfirewall

дополнительные сведения об использовании средств для настройки параметров брандмауэра Windows см. в разделе [начало работы с Windows брандмауэром в расширенной безопасности](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748991(v=ws.10)).

 

 
