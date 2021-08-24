---
description: Метод Ваитевент ожидает, пока заданное событие не будет сигнальным.
ms.assetid: 64880f46-7b8f-4823-9d50-052e30ecf04b
title: Кдинамикаутпутпин. Ваитевент, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.WaitEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3797c9127d3e931cd64fa35e822eac3151acc7fa1a8c4c0c9e93d6a36c0dfe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871934"
---
# <a name="cdynamicoutputpinwaitevent-method"></a>Кдинамикаутпутпин. Ваитевент, метод

`WaitEvent`Метод ожидает, пока заданное событие не будет сигнальным.

## <a name="syntax"></a>Синтаксис


```C++
static HRESULT WaitEvent(
   HANDLE hEvent
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*хевент* 
</dt> <dd>

Дескриптор события.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение **HRESULT** . Возможные значения включают в себя, показанные в следующей таблице.



| Код возврата                                                                                  | Описание                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>         | Успешно.<br/>          |
| <dl> <dt>**\_непредвиденная E**</dt> </dl> | Непредвиденная ошибка.<br/> |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кдинамикаутпутпин**](cdynamicoutputpin.md)
</dt> </dl>

 

 




