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
ms.openlocfilehash: 0ab5bc2aabf77fb73739528e99cda7961ae87e9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657775"
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

## <a name="remarks"></a>Комментарии

Для событий автоматического сброса событие сбрасывается в несигнальное состояние, когда этот метод возвращает значение.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Камевент**](camevent.md)
</dt> </dl>

 

 




