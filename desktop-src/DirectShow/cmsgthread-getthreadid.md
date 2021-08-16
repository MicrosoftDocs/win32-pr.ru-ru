---
description: Возвращает идентификатор потока.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Кмсгсреад. Жетсреадид, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3b0837a7f050f09794b06e490f45012e0704e187b02668cd2af2a5bf8edf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214104"
---
# <a name="cmsgthreadgetthreadid-method"></a>Кмсгсреад. Жетсреадид, метод

Возвращает идентификатор потока.

## <a name="syntax"></a>Синтаксис


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Возвращает закрытый элемент данных **\_ потока ThreadId** .

## <a name="remarks"></a>Remarks

Эта функция возвращает идентификатор Microsoft Win32 для рабочего потока. Эту функцию-член можно вызвать либо в рабочем потоке, либо в клиентском потоке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мсгсрд. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




