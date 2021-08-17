---
description: Текущий интервал событий для отчета об административном адресе в миллисекундах.
ms.assetid: 495dd8a1-4244-468f-b295-337b393aea8a
title: Локатиондисп. Цивикаддрессрепортфактори. Репортинтервал, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.CivicAddressReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: d18db71ac97bbfca60d4892bb151388eee97dbb481508b86b595d5dda74954fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387165"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Локатиондисп. Цивикаддрессрепортфактори. Репортинтервал, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте [**Windows. API Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Текущий интервал событий для отчета об административном адресе в миллисекундах.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Значение свойства

Это свойство является **ulong** для чтения и записи.

## <a name="remarks"></a>Remarks

Это значение является запросом для поставщика расположения. Поставщик расположения не требуется для предоставления отчетов по запрошенному вами интервалу. Прочтите значение этого свойства, чтобы определить значение параметра интервала true Report.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | только Windows 7 \[ настольных приложений\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

