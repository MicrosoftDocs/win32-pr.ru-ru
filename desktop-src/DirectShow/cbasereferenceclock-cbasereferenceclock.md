---
description: Метод конструктора Кбасереференцеклокк. Кбасереференцеклокк.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Конструктор Кбасереференцеклокк. Кбасереференцеклокк (Рефклокк. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6ea08e5555aa6286dac80642f19969e6e669a4ec6ccddb4e530d13e0253b4bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954993"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a>Кбасереференцеклокк. Кбасереференцеклокк, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* 
</dt> <dd>

Указатель на строку, содержащую имя объекта. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

</dd> <dt>

*pUnk* 
</dt> <dd>

Указатель на владельца этого объекта. Если объект является агрегатным, передайте указатель на интерфейс IUnknown объекта агрегирования. В противном случае присвойте этому параметру **значение NULL**.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** . При возникновении ошибки метод возвращает код ошибки в этом параметре. Не устанавливайте для этого параметра **значение NULL**.

</dd> <dt>

*псчед* 
</dt> <dd>

Указатель на объект [**камсчедуле**](camschedule.md) . Если **значение равно NULL**, этот метод создает новый объект **камсчедуле** .

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>рефклокк. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




