---
description: Использует функцию Microsoft Win32 Сетсреадприорити для установки нового значения приоритета потока.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: Кмсгсреад. Сетсреадприорити, метод (Мсгсрд. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SetThreadPriority
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cfa3cd81907a251d2acf7129405e187286df3c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669396"
---
# <a name="cmsgthreadsetthreadpriority-method"></a>Кмсгсреад. Сетсреадприорити, метод

Использует функцию Microsoft Win32 **сетсреадприорити** для установки нового значения приоритета потока.

## <a name="syntax"></a>Синтаксис


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*нприорити* 
</dt> <dd>

Приоритет потока.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из следующих значений.



| Код возврата                                                                              | Описание                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | Приоритет был успешно установлен.<br/> |
| <dl> <dt>FALSE * * * *</dt> </dl> | Приоритет не задан.<br/>          |



 

## <a name="remarks"></a>Комментарии

Клиент и рабочий поток могут вызывать эту функцию члена.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мсгсрд. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




