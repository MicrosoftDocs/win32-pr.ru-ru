---
description: Интерфейс беспроводного программирования нерегламентированный компьютер состоит из следующих интерфейсов.
ms.assetid: 8e975750-cfcc-4e36-a3d1-539b7c077459
title: Беспроводные нерегламентированные интерфейсы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcc4fe481a5be1ff428396e5fd9b199f5a291fbe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673489"
---
# <a name="wireless-ad-hoc-interfaces"></a>Беспроводные нерегламентированные интерфейсы

Интерфейс беспроводного программирования нерегламентированный компьютер состоит из следующих интерфейсов.



| Имя_интерфейса                                                                       | Описание                                                                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface)                                 | Представляет адаптер беспроводной сети (NIC).                                                    |
| [**IDot11AdHocInterfaceNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterfacenotificationsink) | Определяет уведомления, поддерживаемые [**IDot11AdHocInterface**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocinterface).           |
| [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager)                                     | Создает и управляет 802,11 нерегламентированных сетей.                                                            |
| [**IDot11AdHocManagerNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanagernotificationsink)     | Определяет уведомления, поддерживаемые интерфейсом [**IDot11AdHocManager**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocmanager) . |
| [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork)                                     | Представляет доступное нерегламентированное назначение сети в пределах диапазона подключений.                            |
| [**IDot11AdHocNetworkNotificationSink**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetworknotificationsink)     | Определяет уведомления, поддерживаемые интерфейсом [**IDot11AdHocNetwork**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocnetwork) . |
| [**IDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-idot11adhocsecuritysettings)                   | Задает параметры безопасности для беспроводной сети "нерегламентированный компьютер".                                         |
| [**IEnumDot11AdHocInterfaces**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocinterfaces)                       | Представляет коллекцию видимых в настоящее время нерегламентированных сетевых интерфейсов 802,11.                       |
| [**IEnumDot11AdHocNetworks**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocnetworks)                           | Представляет коллекцию видимых в настоящее время 802,11 нерегламентированных сетей.                                 |
| [**IEnumDot11AdHocSecuritySettings**](/windows/desktop/api/adhoc/nn-adhoc-ienumdot11adhocsecuritysettings)           | Представляет коллекцию параметров безопасности, связанных с каждой видимой беспроводной сетью нерегламентированных сетей.   |



 

> [!Note]  
> Нерегламентированный режим может быть недоступен в будущих версиях Windows. Начиная с Windows 8.1 и Windows Server 2012 R2, следует использовать [Wi-Fi Direct](about-the-wi-fi-direct-api.md) .

 

 

 



