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
ms.openlocfilehash: cfea481a3f24aee808fffba9be91b1fecf63fce8a875dc056420a8f075b677d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118656409"
---
# <a name="cdynamicoutputpinm_hnotifycallerpinblockedevent-member"></a>Элемент Кдинамикаутпутпин:: m \_ хнотификаллерпинблоккедевент

Событие, сообщающее о том, что ПИН-код успешно заблокирован, или пользователь отменяет незавершенный блок.

## <a name="syntax"></a>Синтаксис


```C++
HANDLE m_hNotifyCallerPinBlockedEvent;
```



## <a name="remarks"></a>Remarks

Прежде чем обращаться к этой переменной, удерживайте критический раздел [**кдинамикаутпутпин:: m \_ блоккстателокк**](cdynamicoutputpin-m-blockstatelock.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




