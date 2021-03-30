---
title: Справочник по API контрольной точки
description: Следующие интерфейсы являются частью API-интерфейса контрольной точки с технологией UPnP. API контрольной точки поддерживает Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic и C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691a0d764f612d957ac11b3b052859f081bc7285
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104329312"
---
# <a name="control-point-api-reference"></a>Справочник по API контрольной точки

Следующие интерфейсы являются частью API-интерфейса контрольной точки с технологией UPnP. API контрольной точки поддерживает Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic и C++.



| Интерфейс                                                                                      | Описание                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**иупнпаддрессфамиликонтрол**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Позволяет приложению получить доступ к флагу семейства адресов объекта Finder устройства.                                                                                                                                          |
| [**иупнпдескриптиондокумент**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Позволяет приложению загрузить описание устройства. Этот интерфейс является надежным для сценариев.                                                                                                                                     |
| [**иупнпдескриптиондокументкаллбакк**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Позволяет приложению принимать результаты асинхронной операции загрузки.                                                                                                                                               |
| [**иупнпдевице**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Позволяет приложению получать сведения о конкретном устройстве.                                                                                                                                                        |
| [**иупнпдевицедокументакцесс**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Позволяет приложению получить URL-адрес документа описания устройства.                                                                                                                                                     |
| [**иупнпдевицедокументакцессекс**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Предоставляет метод для получения всего документа описания каждого устройства в формате XML для конкретного устройства.                                                                                                                                  |
| [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Позволяет приложению найти устройство.                                                                                                                                                                                       |
| [**иупнпдевицефиндераддкаллбакквисинтерфаце**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Позволяет приложению принимать асинхронные результаты поиска от инфраструктуры UPnP вместе с идентификатором GUID сетевого адаптера, через который поступило объявление устройства.                                                  |
| [**иупнпдевицефиндеркаллбакк**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Позволяет приложению принимать асинхронные результаты поиска из инфраструктуры UPnP.                                                                                                                                         |
| [**иупнпдевицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Перечисляет коллекцию устройств.                                                                                                                                                                                            |
| [**иупнфттфеадерконтрол**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Позволяет приложению устанавливать заголовки HTTP "агент пользователя" из экземпляров класса, реализующих интерфейсы [**иупнпдевицефиндер**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) или [**иупнпдескриптиондокумент**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) . |
| [**иупнпсервице**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Позволяет приложению получать сведения о состоянии и вызывать действия для службы.                                                                                                                                         |
| [**иупнпсервицеасинк**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Асинхронно запрашивать переменные состояния и вызывать действия для экземпляра службы.                                                                                                                                           |
| [**иупнпсервицекаллбакк**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Позволяет приложению принимать уведомления от инфраструктуры UPnP при возникновении событий.                                                                                                                                      |
| [**иупнпсервицес**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Перечисляет коллекцию служб.                                                                                                                                                                                           |



 

 

 




