---
description: 'Метод Жетрекуессандле извлекает дескриптор события, сигнального методом Камсреад:: Каллворкер.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Камсреад. Жетрекуессандле, метод (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 82fa1be333ff35821f187cea980746c6b729a05c12e2103f4465bb44bbcc6f9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652594"
---
# <a name="camthreadgetrequesthandle-method"></a>Камсреад. Жетрекуессандле, метод

`GetRequestHandle`Метод получает дескриптор события, сигнальное методом [**камсреад:: каллворкер**](camthread-callworker.md) .

## <a name="syntax"></a>Синтаксис


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает маркер события.

## <a name="remarks"></a>Remarks

Класс Камевент сохраняет закрытое событие ручного сброса, которое задается Каллворкер и сбрасывается методом [**камсреад:: Reply**](camthread-reply.md) .

При вызове функции, такой как WaitForMultipleObjects, используйте Жетрекуессандле для получения маркера события.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




