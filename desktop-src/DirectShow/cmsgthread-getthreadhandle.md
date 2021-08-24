---
description: Получает маркер для потока в объекте Кмсгсреад.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Кмсгсреад. Жетсреадхандле, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ecb968156302c4fd1a8c48d1c6f3175977059298d2f6af5207abc376a6e107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585694"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>Кмсгсреад. Жетсреадхандле, метод

Получает маркер для потока в объекте [**кмсгсреад**](cmsgthread.md) .

## <a name="syntax"></a>Синтаксис


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает обработчик потока.

## <a name="remarks"></a>Remarks

Этот поток может быть передан в функции ожидания, например [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects). Дескриптор потока получает сигнал при завершении потока.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мсгсрд. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

