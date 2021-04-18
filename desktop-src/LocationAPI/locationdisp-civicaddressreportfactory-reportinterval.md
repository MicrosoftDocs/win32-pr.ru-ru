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
ms.openlocfilehash: 47f7840be20ac640b5a8e7014f8401bc2350d328
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684551"
---
# <a name="locationdispcivicaddressreportfactoryreportinterval-property"></a>Локатиондисп. Цивикаддрессрепортфактори. Репортинтервал, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Текущий интервал событий для отчета об административном адресе в миллисекундах.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
ReportInterval = LocationDisp.CivicAddressReportFactory.ReportInterval
LocationDisp.CivicAddressReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Значение свойства

Это свойство является **ulong** для чтения и записи.

## <a name="remarks"></a>Комментарии

Это значение является запросом для поставщика расположения. Поставщик расположения не требуется для предоставления отчетов по запрошенному вами интервалу. Прочтите значение этого свойства, чтобы определить значение параметра интервала true Report.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

