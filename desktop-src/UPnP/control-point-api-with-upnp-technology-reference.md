---
title: Справочник по API контрольной точки
description: Следующие интерфейсы являются частью API-интерфейса контрольной точки с технологией UPnP. API контрольной точки поддерживает microsoft Visual Basic scripting Edition (VBScript), microsoft Visual Basic и C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b3dab16874ebeb7b43ef1e8cf28def13d3ef1d7169a5aae4836b39da66636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058122"
---
# <a name="control-point-api-reference"></a>Справочник по API контрольной точки

Следующие интерфейсы являются частью API-интерфейса контрольной точки с технологией UPnP. API контрольной точки поддерживает microsoft Visual Basic scripting Edition (VBScript), microsoft Visual Basic и C++.



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



 

 

 




