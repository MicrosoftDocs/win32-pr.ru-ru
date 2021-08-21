---
description: Обработчик для потока.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: 'Элемент Камсреад:: m_hThread (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7293a97373a53d102887e5958c4296aff3dcfe3d392c80492ed773af62a8f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158915"
---
# <a name="camthreadm_hthread-member"></a>Элемент Камсреад:: m \_ хсреад

Обработчик для потока.

## <a name="syntax"></a>Синтаксис


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Remarks

Эта переменная инициализируется как **null**. Метод [**камсреад:: Create**](camthread-create.md) присваивает этой переменной значение обработчика потока. Чтобы определить, существует ли поток, вызовите метод [**камсреад:: среадексистс**](camthread-threadexists.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Камсреад**](camthread.md)
</dt> </dl>

 

 




