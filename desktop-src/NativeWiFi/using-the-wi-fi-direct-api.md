---
description: Показывает, как использовать Wi-Fi прямые функции в классических приложениях.
ms.assetid: 50B95B7D-B860-44DF-8E78-1E7D2DC5A9B6
title: Использование прямых функций Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8850f5b278a158e32f78118cf5d0d408c123192e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105663040"
---
# <a name="using-the-wi-fi-direct-functions"></a>Использование прямых функций Wi-Fi

В этом разделе показано, как использовать Wi-Fi прямые функции в классических приложениях. Начиная с Windows 8 и Windows Server 2012, Wi-Fi прямые функции были добавлены в собственный интерфейс API WiFi.

Функция Wi-Fi Direct основана на разработке Wi-Fi технической спецификации v 1.1 в Wi-Fi Alliance (см. статью [опубликованные спецификации Wi-Fi Alliance](https://www.wi-fi.org/)). Целью Wi-Fiной технической спецификации является предоставление решения для Wi-Fi подключения устройства к устройству без необходимости использовать беспроводную точку доступа (беспроводной доступ) для настройки подключения или использования существующего механизма Wi-Fi ad hoc (ИБСС).

> [!Note]  
> Нерегламентированный режим может быть недоступен в будущих версиях Windows. Начиная с Windows 8.1 и Windows Server 2012 R2 используйте вместо них Wi-Fi Direct.

 

Следующие функции поддерживают функцию прямого Wi-Fi.

-   [**Вфдканцелопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) — указывает, что приложению требуется отменить отложенную функцию [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) , которая не была завершена.
-   [**Вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) — закрывает обработчик для Wi-Fi Direct Service.
-   [**Вфдклосесессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) — закрывает сеанс после предыдущего успешного вызова функции [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**Вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) — открывает обработчик для Wi-Fi Direct Service и согласовывает версию интерфейса API прямого подключения Wi-Fi для использования.
-   [**Вфдопенлегацисессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) — извлекает и применяет сохраненный профиль для устройства Wi-Fi Direct.
-   [**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) — запускает подключение по требованию к конкретному Wi-Fi прямое устройство, которое ранее было парно с помощью связывания Windows.
-   [**Вфдупдатедевицевисибилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) — обновляет видимость устройства для Wi-Fi адресом прямого устройства для заданного установленного Wi-Fi прямого узла устройства.
-   [**WFD \_ \_ \_ \_ Обратный вызов для завершения открытия сеанса**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) — определяет функцию обратного вызова, вызываемую функцией [**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) по завершении операции **вфдстартопенсессион**

Для классического приложения функция Wi-Fi Direct требует, чтобы устройства Wi-FI Direct были ранее парными для пользователя с помощью пользовательского интерфейса связывания Windows. После завершения связывания сохраняется профиль, который позволяет использовать Wi-Fi прямые функции для запуска Wi-Fi прямого сеанса для установления соединения между Wi-Fiными устройствами.

Чтобы использовать Wi-Fi Direct, приложение должно сначала получить обработчик прямой службы Wi-Fi, вызвав функцию [**вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) . Wi-Fi Direct (WFD), возвращаемый функцией **вфдопенхандле** , используется для последующего Wi-Fi прямых вызовов функций, выполненных в Wi-Fi Direct Service.

Функция [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) запускает асинхронную операцию для запуска подключения по требованию к конкретному Wi-Fi непосредственному устройству. Целевое устройство Wi-Fi должно быть ранее сопряжено с помощью функции связывания Windows. По завершении асинхронной операции вызывается функция обратного вызова, указанная в параметре *пфнкаллбакк* .

После того как приложение будет выполнено с помощью Wi-Fi Direct Service, приложение должно вызвать функцию [**вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) , чтобы сообщить Wi-Fi прямой службе о том, что приложение выполняется с помощью службы. Это позволяет службе Wi-Fi Direct Service выпустить ресурсы, используемые приложением.

Дополнительные сведения о Wi-Fi Direct для использования в приложениях для Магазина Windows см. в разделе [**пирфиндер**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) и связанные классы в пространстве имен [**Windows. Networking. близость**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>См. также

<dl> <dt>

**Другие источники**
</dt> <dt>

[О встроенных WiFi](about-native-wifi.md)
</dt> <dt>

[Сведения о встроенном API Wi-Fi](about-the-native-wifi-api.md)
</dt> <dt>

[О функции Direct Wi-Fi](about-the-wi-fi-direct-api.md)
</dt> <dt>

**Ссылки**
</dt> <dt>

[**пирфиндер**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041)
</dt> <dt>

[**\_ \_ \_ обратный вызов для завершения открытого сеанса \_ WFD**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
</dt> <dt>

[**вфдканцелопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
</dt> <dt>

[**вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
</dt> <dt>

[**вфдклосесессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
</dt> <dt>

[**вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
</dt> <dt>

[**вфдопенлегацисессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
</dt> <dt>

[**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
</dt> <dt>

[**вфдупдатедевицевисибилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)
</dt> <dt>

[**Windows.Networking.Proximity**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041)
</dt> </dl>

 

 
