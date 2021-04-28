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
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119942"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Рефклокк. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасереференцеклокк**](cbasereferenceclock.md)
</dt> </dl>

 

 




