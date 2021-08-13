---
description: 'Если вы используете COM API для WMI для извлечения или хранения сведений о локализованном классе, укажите языковой стандарт в параметре Стрлокале для интерфейса Ивбемлокатор:: Коннектсервер.'
ms.assetid: 940a7bd9-c2ea-4deb-b5d8-207a0ce7a616
ms.tgt_platform: multiple
title: Получение измененных классов с помощью API COM для WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3752be42a7111e677e7cd60e0bfe9996350f9ae19e7bd0e168d1fa5da82fe42a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554028"
---
# <a name="retrieving-amended-classes-using-the-com-api-for-wmi"></a>Получение измененных классов с помощью API COM для WMI

Если вы используете COM API для WMI для извлечения или хранения сведений о локализованном классе, укажите языковой стандарт в параметре *стрлокале* для интерфейса [**Ивбемлокатор:: коннектсервер**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemlocator-connectserver) . При чтении или записи измененных классов укажите, что вы хотите использовать локализованные определения классов, указав \_ флаг \_ WBEM \_ . в \_ качестве флага для параметра *ифлагс* следует использовать измененные квалификаторы.

В следующей таблице перечислены синхронные и асинхронные версии методов, использующих \_ флаг WBEM \_ , \_ флаг измененных \_ квалификаторов.



| Синхронный метод                                                            | Асинхронный метод                                                                     |
|-------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| [**IWbemServices:: Креатеклассенум**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenum)       | [**IWbemServices:: Креатеклассенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)       |
| [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) | [**IWbemServices:: Креатеинстанцеенумасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) |
| [**IWbemServices:: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery)                   | [**IWbemServices:: Ексеккуерясинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync)                   |
| [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject)                   | [**IWbemServices:: Жетобжектасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)                   |
| [**IWbemServices::P Уткласс**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclass)                     | [**IWbemServices::P Утклассасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putclassasync)                     |
| [**IWbemServices::P Утинстанце**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstance)               | [**IWbemServices::P Утинстанцеасинк**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-putinstanceasync)               |



 

 

 



