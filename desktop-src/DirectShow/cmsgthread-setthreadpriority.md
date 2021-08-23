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
ms.openlocfilehash: ce293f32f765a89451ecf07b4532afc5fc4a7a132287d5b09b54962f93135215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585674"
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



 

## <a name="remarks"></a>Remarks

Клиент и рабочий поток могут вызывать эту функцию члена.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мсгсрд. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмсгсреад**](cmsgthread.md)
</dt> </dl>

 

 




