---
title: Макросы оболочки Трацелоггинг
description: Содержит список макросов-оболочек для поставщиков Трацелоггинг.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779688"
---
# <a name="tracelogging-wrapper-macros"></a>Макросы оболочки Трацелоггинг

Содержит список макросов-оболочек для поставщиков Трацелоггинг.

Для записи событий с помощью поставщиков Трацелоггинг необходимо использовать макросы записи Трацелоггинг [**трацелоггингврите**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) или [**трацелоггингвритеактивити**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity). Для обоих этих макросов требуется заключить данные событий в макрос оболочки. Существует несколько различных макросов-оболочек для различных типов данных. Полный список макросов Трацелоггинг см. в разделе [макросы трацелоггинг](trace-logging-macros.md).

Помимо макросов оболочки, приведенных выше, для отдельных типов данных доступны несколько макросов. Все эти макросы имеют тот же формат, что и макрос [трацелоггингвалуе](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) . Можно использовать макрос Трацелоггингвалуе для автоматического определения нужного макроса-оболочки или непосредственного использования конкретного макроса.

-   [**трацелоггингбинари**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [**трацелоггингчаннел**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [**трацелоггингкустоматтрибуте**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [**трацелоггингдескриптион**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [**трацелоггинжевенттаг**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [**трацелоггингкэйворд**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [**трацелоггинглевел**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [**трацелоггингопкоде**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [**трацелоггингсоккетаддресс**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [**трацелоггингструкт**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [**трацелоггингвалуе**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> **Трацелоггингоптионграуп** специально предназначен для использования внутри трацелоггинг \_ определения \_ поставщика.
>
> -   [**трацелоггингоптионграуп**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

Ниже приведены отдельные макросы-оболочки.

-   TraceLoggingInt8

-   TraceLoggingUInt8

-   TraceLoggingInt16

-   TraceLoggingUInt16

-   TraceLoggingInt32

-   TraceLoggingUInt32

-   TraceLoggingInt64

-   TraceLoggingUInt64

-   TraceLoggingFloat32

-   TraceLoggingFloat64

-   трацелоггингбул

-   трацелоггингфилетиме

-   трацелоггинггуид

-   трацелоггингпоинтер

-   трацелоггингсистемтиме

-   TraceLoggingHexInt8

-   TraceLoggingHexUInt8

-   TraceLoggingHexInt32

-   TraceLoggingHexUInt32

-   TraceLoggingHexInt64

-   TraceLoggingHexUInt64

-   трацелоггингвчар

-   трацелоггингчар

-   трацелоггингинтптр

-   трацелоггингуинтптр

-   трацелоггингбулеан

-   TraceLoggingHexInt16

-   TraceLoggingHexUInt16

-   трацелоггингпид

-   трацелоггингтид

-   трацелоггингпорт

-   трацелоггингвинеррор

-   трацелоггингнтстатус

-   трацелоггингхресулт

-   трацелоггингсоккетаддресс

-   трацелоггингсид

-   трацелоггингстринг

-   трацелоггингвидестринг

-   трацелоггингкаунтедстринг

-   трацелоггингкаунтедвидестринг

-   трацелоггингансистринг

-   трацелоггингуникодестринг

-   Трацелоггингбинари (пустые \* данные, размер данных в байтах, \[ необязательное \] имя) параметры этого макроса отличаются от указанных выше. Если указан параметр *Name* , он должен быть строковым литералом (а не переменной) и не может содержать внедренные символы NULL. Если параметр *Name* не указан, имя создается автоматически.

API Трацелоггинг также делает несколько макросов доступными для массивов. Эти массивы могут иметь фиксированную длину или иметь переменную длину в зависимости от того, какой макрос оболочки вы решили использовать. Все эти макросы-оболочки соответствуют этому формату.

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

Параметр *пвалс* указывает на массив данных, а *квалс* указывает количество элементов в массиве. *квалс* должен быть константой и не может быть переменной. Как и в случае с макросами одного значения, *Name*, **DESC** и *Tags* являются необязательными параметрами и должны следовать тем же ограничениям, которые описаны в макросе **трацелоггингвалуе** .

-   TraceLoggingInt8FixedArray

-   TraceLoggingUInt8FixedArray

-   TraceLoggingInt16FixedArray

-   TraceLoggingUInt16FixedArray

-   TraceLoggingInt32FixedArray

-   TraceLoggingUInt32FixedArray

-   TraceLoggingInt64FixedArray

-   TraceLoggingUInt64FixedArray

-   TraceLoggingFloat32FixedArray

-   TraceLoggingFloat64FixedArray

-   трацелоггингбулфикседаррай

-   трацелоггинггуидфикседаррай

-   трацелоггингпоинтерфикседаррай

-   трацелоггингфилетимефикседаррай

-   трацелоггингсистемтимефикседаррай

-   TraceLoggingHexInt8FixedArray

-   TraceLoggingHexUInt8FixedArray

-   TraceLoggingHexInt32FixedArray

-   TraceLoggingHexUInt32FixedArray

-   TraceLoggingHexInt64FixedArray

-   TraceLoggingHexUInt64FixedArray

-   трацелоггингвчарфикседаррай

-   трацелоггингчарфикседаррай

-   трацелоггингинтптрфикседаррай

-   трацелоггингуинтптрфикседаррай

-   трацелоггингбулеанфикседаррай

-   TraceLoggingHexInt16FixedArray

-   TraceLoggingHexUInt16FixedArray

-   TraceLoggingInt8Array

-   TraceLoggingUInt8Array

-   TraceLoggingInt16Array

-   TraceLoggingUInt16Array

-   TraceLoggingInt32Array

-   TraceLoggingUInt32Array

-   TraceLoggingInt64Array

-   TraceLoggingUInt64Array

-   TraceLoggingFloat32Array

-   TraceLoggingFloat64Array

-   трацелоггингбуларрай

-   трацелоггинггуидаррай

-   трацелоггингпоинтераррай

-   трацелоггингфилетимеаррай

-   трацелоггингсистемтимеаррай

-   TraceLoggingHexInt8Array

-   TraceLoggingHexUInt8Array

-   TraceLoggingHexInt32Array

-   TraceLoggingHexUInt32Array

-   TraceLoggingHexInt64Array

-   TraceLoggingHexUInt64Array

-   трацелоггингвчараррай

-   трацелоггингчараррай

-   трацелоггингинтптраррай

-   трацелоггингуинтптраррай

-   трацелоггингбулеанаррай

-   TraceLoggingHexInt16Array

-   TraceLoggingHexUInt16Array

 

 




