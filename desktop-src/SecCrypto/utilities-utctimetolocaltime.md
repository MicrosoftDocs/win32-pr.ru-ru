---
description: Преобразует время в формате UTC (время по Гринвичу) в местное время компьютера.
ms.assetid: 4085d7cb-d346-477d-a043-e96fb951c35a
title: Метод Utilities. Утктиметолокалтиме
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Utilities.UTCTimeToLocalTime
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: fe41cf8d9ec92c0c71be5130aded0b7db539b9b1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685023"
---
# <a name="utilitiesutctimetolocaltime-method"></a>Метод Utilities. Утктиметолокалтиме

\[Метод **утктиметолокалтиме** доступен для использования в операционных системах, указанных в разделе требования.\]

Метод **утктиметолокалтиме** преобразует всеобщее скоординированное время (время по Гринвичу) в местное время компьютера.

## <a name="syntax"></a>Синтаксис


```VB
Utilities.UTCTimeToLocalTime( _
  ByVal UTCTime _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Утктиме* \[ окне\]
</dt> <dd>

Время в формате UTC, которое необходимо преобразовать в местное время компьютера.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Местное время, соответствующее заданному всеобщему скоординированному времени.

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

 

 




