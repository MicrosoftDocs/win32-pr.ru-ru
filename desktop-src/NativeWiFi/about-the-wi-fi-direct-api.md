---
description: Собственный API Wi-Fi содержит набор функций, которые поддерживают использование Wi-Fi Direct для классических приложений.
ms.assetid: A649EBBA-1076-4426-9C4D-85AB8C415C66
title: О функции Direct Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e503cb2bf86f81904b1c85c2bdf96b66c0762e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674300"
---
# <a name="about-the-wi-fi-direct-feature"></a>О функции Direct Wi-Fi

Собственный API Wi-Fi содержит набор функций, которые поддерживают использование Wi-Fi Direct для классических приложений. Начиная с Windows 8 и Windows Server 2012, Wi-Fi прямые функции были добавлены в собственный интерфейс API WiFi.

Функция Wi-Fi Direct основана на разработке Wi-Fi технической спецификации v 1.1 в Wi-Fi Alliance (см. статью [опубликованные спецификации Wi-Fi Alliance](https://www.wi-fi.org/)). Целью Wi-Fiной технической спецификации является предоставление решения для Wi-Fi подключения устройства к устройству без необходимости использовать беспроводную точку доступа (беспроводной доступ) для настройки подключения или использования существующего механизма Wi-Fi ad hoc (ИБСС).

> [!Note]  
> Нерегламентированный режим может быть недоступен в будущих версиях Windows. Начиная с Windows 8.1 и Windows Server 2012 R2 используйте вместо них Wi-Fi Direct.

 

Для классического приложения функция Wi-Fi Direct требует, чтобы устройства Wi-FI Direct были ранее парными для пользователя с помощью пользовательского интерфейса связывания Windows. После завершения связывания сохраняется профиль, который позволяет использовать Wi-Fi прямые функции для запуска Wi-Fi прямого сеанса для установления соединения между Wi-Fiными устройствами.

Следующие функции поддерживают функцию прямого Wi-Fi.

-   [**Вфдканцелопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession) — указывает, что приложению требуется отменить отложенную функцию [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) , которая не была завершена.
-   [**Вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle) — закрывает обработчик для Wi-Fi Direct Service.
-   [**Вфдклосесессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession) — закрывает сеанс после предыдущего успешного вызова функции [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) .
-   [**Вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle) — открывает обработчик для Wi-Fi Direct Service и согласовывает версию интерфейса API прямого подключения Wi-Fi для использования.
-   [**Вфдопенлегацисессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession) — извлекает и применяет сохраненный профиль для устройства Wi-Fi Direct.
-   [**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) — запускает подключение по требованию к конкретному Wi-Fi прямое устройство, которое ранее было парно с помощью связывания Windows.
-   [**Вфдупдатедевицевисибилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility) — обновляет видимость устройства для Wi-Fi адресом прямого устройства для заданного установленного Wi-Fi прямого узла устройства.
-   [**WFD \_ \_ \_ \_ Обратный вызов для завершения открытия сеанса**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback) — определяет функцию обратного вызова, вызываемую функцией [**Вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession) по завершении операции **вфдстартопенсессион**

Дополнительные сведения об использовании Wi-Fi Direct в классическом приложении см. в разделе [Использование функций Wi-Fi Direct](using-the-wi-fi-direct-api.md).

Дополнительные сведения о Wi-Fi Direct для использования в приложениях для Магазина Windows см. в разделе [**пирфиндер**](/uwp/api/Windows.Networking.Proximity.PeerFinder?view=winrt-19041) и связанные классы в пространстве имен [**Windows. Networking. близость**](/uwp/api/Windows.Networking.Proximity?view=winrt-19041) .

## <a name="related-topics"></a>См. также

<dl> <dt>

**Другие источники**
</dt> <dt>

[О встроенных WiFi](about-native-wifi.md)
</dt> <dt>

[Сведения о встроенном API Wi-Fi](about-the-native-wifi-api.md)
</dt> <dt>

[Сведения о беспроводном нерегламентированном API](about-the-wireless-ad-hoc-api.md)
</dt> <dt>

[Использование прямых функций Wi-Fi](using-the-wi-fi-direct-api.md)
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

 

 
