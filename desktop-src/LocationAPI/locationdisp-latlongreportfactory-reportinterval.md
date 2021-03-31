---
description: Текущий интервал событий для отчета широты и долготы в миллисекундах.
ms.assetid: bb33c4c1-805d-4519-8363-b0221d420b36
title: Локатиондисп. Латлонгрепортфактори. Репортинтервал, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.ReportInterval
api_type:
- COM
api_location: ''
ms.openlocfilehash: b456f69a70655b22b1eca30e02d9d5369d19f38c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265051"
---
# <a name="locationdisplatlongreportfactoryreportinterval-property"></a>Локатиондисп. Латлонгрепортфактори. Репортинтервал, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Текущий интервал событий для отчета широты и долготы в миллисекундах.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```JScript
ReportInterval = LocationDisp.LatLongReportFactory.ReportInterval
LocationDisp.LatLongReportFactory.ReportInterval = ReportInterval
```



## <a name="property-value"></a>Значение свойства

Это свойство является **ulong** для чтения и записи.

## <a name="remarks"></a>Комментарии

Это значение является запросом к поставщику расположения. Поставщик расположения не требуется для предоставления отчетов на запрошенный интервал. Прочтите значение этого свойства, чтобы определить значение параметра интервала true Report.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

