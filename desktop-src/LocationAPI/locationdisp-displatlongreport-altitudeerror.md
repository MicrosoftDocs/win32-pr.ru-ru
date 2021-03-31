---
description: Ошибка высоты, в метрах.
ms.assetid: 36ebb079-26e6-4b3f-ad73-547a47bd23d7
title: Локатиондисп. Дисплатлонгрепорт. Алтитудиррор, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.DispLatLongReport.AltitudeError
api_type:
- COM
api_location: ''
ms.openlocfilehash: 92fd71b133912a57e6ed4ef034dda6fe92ef9b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910991"
---
# <a name="locationdispdisplatlongreportaltitudeerror-property"></a>Локатиондисп. Дисплатлонгрепорт. Алтитудиррор, свойство

\[Объектная модель API расположения доступна для использования в операционных системах, указанных в разделе требования. В последующих версиях он может быть изменен или недоступен. Вместо этого для доступа к расположению с веб-сайта используйте [API географического расположения W3C](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)). Чтобы получить доступ к расположению из классического приложения, используйте API [**Windows. Devices. Географическое расположение**](/uwp/api/Windows.Devices.Geolocation) .\]

Ошибка высоты, в метрах.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
AltitudeError = LocationDisp.DispLatLongReport.AltitudeError
```



## <a name="property-value"></a>Значение свойства

Это свойство доступно только для чтения ( **число** с плавающей запятой двойной точности).

## <a name="remarks"></a>Комментарии

Датчики расположения не являются обязательными для предоставления этого свойства. При попытке доступа к этому свойству следует обращаться к исключениям.

## <a name="examples"></a>Примеры

Пример использования этого свойства см. [в примере простого отчета LatLong](/uwp/api/Windows.Devices.Geolocation).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 7\]<br/> |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                  |



 

