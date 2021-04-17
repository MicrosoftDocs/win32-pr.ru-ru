---
description: Событие, сообщающее о том, что ПИН-код успешно заблокирован, или пользователь отменяет незавершенный блок.
ms.assetid: 699bb7f7-e4f7-47c3-bbb1-0bc6556651ae
title: 'Элемент Кдинамикаутпутпин:: m_hNotifyCallerPinBlockedEvent (Амфилтер. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hNotifyCallerPinBlockedEvent
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e28aa890e15602376b9500243a89e8f0e3d3bb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665247"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>Элемент Кдинамикаутпутпин:: m \_ хнотификаллерпинблоккедевент

Событие, сообщающее о том, что ПИН-код успешно заблокирован, или пользователь отменяет незавершенный блок.

## <a name="syntax"></a>Синтаксис


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Примечания

Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




