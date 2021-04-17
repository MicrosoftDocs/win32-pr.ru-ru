---
description: Преобразует местное время компьютера в формат UTC (время по Гринвичу).
ms.assetid: ff5d40ba-7d94-4f11-9c18-e41752d1d7b9
title: Метод Utilities. Локалтиметаутктиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.LocalTimeToUTCTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2691e3306a84ce4eff3d73df4b070ba4b65671f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685024"
---
# <a name="utilitieslocaltimetoutctime-method"></a>Метод Utilities. Локалтиметаутктиме

\[Метод **локалтиметаутктиме** доступен для использования в операционных системах, указанных в разделе требования.\]

Метод **локалтиметаутктиме** Преобразует местное время компьютера в формат UTC (время по Гринвичу).

## <a name="syntax"></a>Синтаксис


```VB
Utilities.LocalTimeToUTCTime( _
  ByVal LocalTime _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Localtime* \[ окне\]
</dt> <dd>

Местное время для преобразования в время в формате UTC.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Время в формате UTC, соответствующее указанному местному времени.

## <a name="remarks"></a>Комментарии

Несмотря на то, что система использует координированное всемирное время, приложения обычно отображают местное время, которое представляет собой дату и время суток для местного часового пояса компьютера.

## <a name="requirements"></a>Требования



| Требование | Значение |
|----------------------------|----------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Служебные программы**](utilities.md)
</dt> </dl>

 

 




