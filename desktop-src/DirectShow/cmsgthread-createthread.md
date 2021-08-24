---
description: Создает поток.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Метод Кмсгсреад. CreateThread (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831874"
---
# <a name="cmsgthreadcreatethread-method"></a>Кмсгсреад. CreateThread, метод

Создает поток.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                              | Описание                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | Поток успешно создан.<br/>     |
| <dl> <dt>FALSE * * * *</dt> </dl> | Не удалось создать поток.<br/> |



 

## <a name="remarks"></a>Remarks

Поток выполняет цикл, блокируется до постановки запроса в очередь (с помощью функции-члена [**кмсгсреад::P утсреадмсг**](cmsgthread-putthreadmsg.md) ), а затем вызывает функцию-член [**Кмсгсреад:: среадмессажепрок**](cmsgthread-threadmessageproc.md) с каждым сообщением.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мсгсрд. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




