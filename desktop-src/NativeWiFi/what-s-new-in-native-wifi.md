---
description: Новые возможности системной поддержки Wi-Fi
ms.assetid: 76d60b95-a34a-4747-b0fa-9230aa60bd63
title: Новые возможности системной поддержки Wi-Fi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a9430fa2c1645d574f8b4ab851a8cf5ce1407139cfe63a6aabeb3ebfd57abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064864"
---
# <a name="whats-new-in-native-wifi"></a>Новые возможности системной поддержки Wi-Fi

## <a name="windows-10-version-2004"></a>Windows 10 версии 2004

См. статью о [подготовке профиля Wi-Fi через веб-сайт](prov-wifi-profile-via-website.md).

## <a name="windows-10"></a>Windows 10,

В [ \_ схему профиля WLAN](wlan-profileschema-schema.md)добавлена поддержка Hotspot 2,0. Hotspot 2,0 обеспечивает автоматическое подключение к общедоступным службам Wi-Fi, используя существующие учетные данные и членство в сетях поставщиков услуг. Поставщики услуг указывают, как соединения устанавливаются с помощью новых элементов схемы, чтобы описать используемые сети и способ проверки подлинности в них. Дополнительные сведения см. в документации по элементу [**Hotspot2**](wlan-profileschema-hotspot2-element.md) .

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 и Windows Server 2012

следующие функции были добавлены в собственные интерфейсы api Wifi на Windows 8 и Windows Server 2012.

Wi-Fi Direct, основанный на разработке Wi-Fiной технической спецификации v 1.1 с помощью Wi-Fi Alliance (см. Описание [опубликованных спецификаций Wi-Fi Alliance](https://www.wi-fi.org/)). Целью Wi-Fiной технической спецификации является предоставление решения для Wi-Fi подключения устройства к устройству без необходимости использовать беспроводную точку доступа (беспроводный ТД) для настройки подключения или использования существующего механизма нерегламентированных Wi-Fi (ИБСС).

Следующие функции поддерживают функцию прямого Wi-Fi.

-   [**\_ \_ \_ обратный вызов для завершения открытого сеанса \_ WFD**](/windows/desktop/api/wlanapi/nc-wlanapi-wfd_open_session_complete_callback)
-   [**вфдканцелопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdcancelopensession)
-   [**вфдклосехандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosehandle)
-   [**вфдклосесессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdclosesession)
-   [**вфдопенхандле**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenhandle)
-   [**вфдопенлегацисессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdopenlegacysession)
-   [**вфдстартопенсессион**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdstartopensession)
-   [**вфдупдатедевицевисибилити**](/windows/desktop/api/wlanapi/nf-wlanapi-wfdupdatedevicevisibility)

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 и Windows Server 2008 R2

следующие функции были добавлены в собственные интерфейсы api Wifi на Windows 7 и Windows Server 2008 R2.

Беспроводная размещенная сеть позволяет одному физическому беспроводному адаптеру подключаться в качестве клиента к точке доступа к оборудованию (AP), в то же время действуя как программный AP, что позволяет другим устройствам, поддерживающим беспроводное подключение, подключаться к нему.

Следующие функции поддерживают функцию беспроводной размещенной сети.

-   [**вланхостеднетворкфорцестарт**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestart)
-   [**вланхостеднетворкфорцестоп**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkforcestop)
-   [**вланхостеднетворкинитсеттингс**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkinitsettings)
-   [**вланхостеднетворккуерипроперти**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkqueryproperty)
-   [**вланхостеднетворккуерисекондарикэй**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerysecondarykey)
-   [**вланхостеднетворккуеристатус**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkquerystatus)
-   [**вланхостеднетворкрефрешсекуритисеттингс**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkrefreshsecuritysettings)
-   [**вланхостеднетворксетпроперти**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetproperty)
-   [**вланхостеднетворксетсекондарикэй**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworksetsecondarykey)
-   [**вланхостеднетворкстартусинг**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstartusing)
-   [**вланхостеднетворкстопусинг**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanhostednetworkstopusing)
-   [**вланрегистервиртуалстатионнотификатион**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanregistervirtualstationnotification)

Следующие новые структуры работают с беспроводной размещенной сетью.

-   [**\_ \_ \_ Параметры сетевого подключения \_ , размещенного в беспроводной сети**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_connection_settings)
-   [**\_ \_ \_ \_ изменение состояния однорангового узла данных в \_ сети WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_data_peer_state_change)
-   [**\_ \_ \_ состояние одноранговой сети в размещенной WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_peer_state)
-   [**\_ \_ состояние радио для сети, РАЗМЕЩЕНной WLAN \_ \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_radio_state)
-   [**\_ \_ \_ Параметры безопасности сети, РАЗМЕЩЕНной в WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_security_settings)
-   [**\_ \_ \_ изменение состояния РАЗМЕЩЕНной сети WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_state_change)
-   [**\_состояние размещенной \_ сети WLAN \_**](/windows/desktop/api/Wlanapi/ns-wlanapi-wlan_hosted_network_status)

Ниже перечислены новые перечисления, которые работают с беспроводной размещенной сетью.

-   [**\_ \_ \_ код уведомления РАЗМЕЩЕНной сети WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_notification_code)
-   [**\_ \_ код операции размещенной сети WLAN \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_opcode)
-   [**\_ \_ \_ \_ состояние проверки подлинности однорангового узла беспроводной сети \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_peer_auth_state)
-   [**\_Причина размещения \_ сети \_ WLAN**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_reason)
-   [**состояние сети, в которой \_ размещена беспроводная \_ сеть \_**](/windows/desktop/api/Wlanapi/ne-wlanapi-wlan_hosted_network_state)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Сведения о беспроводной размещенной сети](about-the-wireless-hosted-network.md)
</dt> <dt>

[Использование беспроводной размещенной сети и общего доступа к подключению к Интернету](using-hosted-network-and-internet-connection-sharing.md)
</dt> </dl>

 

 



