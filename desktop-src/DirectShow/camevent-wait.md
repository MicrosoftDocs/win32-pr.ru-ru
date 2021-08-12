---
description: Метод Wait блокируется до получения сигнала о событии или до истечения времени ожидания.
ms.assetid: bcc13723-a59b-4e8a-bfc8-eadb6facf116
title: Метод Камевент. Wait (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Wait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3875647cb93619e8326066bc9af7a6f99f79a0b0a2df58f668b1e365fd39102b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662515"
---
# <a name="cameventwait-method"></a>Камевент. Wait, метод

`Wait`Метод блокируется до получения сигнала о событии или до истечения времени ожидания.

## <a name="syntax"></a>Синтаксис


```C++
BOOL Wait(
   DWORD dwTimeout = INFINITE
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*двтимеаут* 
</dt> <dd>

Необязательное значение времени ожидания, представленное в миллисекундах.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если событие имеет сигнальное состояние. В противном случае возвращает **значение false**.

## <a name="remarks"></a>Remarks

Для событий автоматического сброса событие сбрасывается в несигнальное состояние, когда этот метод возвращает значение.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камевент**](camevent.md)
</dt> </dl>

 

 




