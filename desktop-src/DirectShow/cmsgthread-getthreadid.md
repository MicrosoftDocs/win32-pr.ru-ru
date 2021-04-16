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
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668657"
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

## <a name="remarks"></a>Комментарии

Эта функция возвращает идентификатор Microsoft Win32 для рабочего потока. Эту функцию-член можно вызвать либо в рабочем потоке, либо в клиентском потоке.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мсгсрд. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




