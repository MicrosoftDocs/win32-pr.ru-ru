---
description: Переменная- \_ член m бусингимажеаллокатор указывает, является ли распределитель для соединения с закреплением объектом Цимажеаллокатор. Если значение равно TRUE, распределитель является объектом Цимажеаллокатор (или производным от этого класса).
ms.assetid: 8eddcab6-77b9-4c8f-be74-33e91661430d
title: 'Элемент Кдравимаже:: m_bUsingImageAllocator (Винутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bUsingImageAllocator
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bf60184758598872577e0c6b293f8eb0b72c5bf7305f1516a4dd6b5a4a639b94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657116"
---
# <a name="cdrawimagem_busingimageallocator-member"></a>Элемент Кдравимаже:: m \_ бусингимажеаллокатор

`m_bUsingImageAllocator`Переменная-член указывает, является ли распределитель для соединения с закреплением объектом **Цимажеаллокатор** . Если значение равно **true**, распределитель является объектом **Цимажеаллокатор** (или производным от этого класса).

## <a name="syntax"></a>Синтаксис


```C++
BOOL m_bUsingImageAllocator;
```



## <a name="remarks"></a>Remarks

Если значение равно **true**, объект **кдравимаже** может использовать функции GDI **BitBlt** и **стретчблт** для отрисовки изображения, а не более медленных функций **сетдибитстодевице** и **стретчдибитс** .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кдравимаже**](cdrawimage.md)
</dt> <dt>

[**Кдравимаже:: Нотифяллокатор**](cdrawimage-notifyallocator.md)
</dt> <dt>

[**Кдравимаже:: Усингимажеаллокатор**](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




