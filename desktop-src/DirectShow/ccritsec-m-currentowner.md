---
description: Идентификатор потока владеющего потока.
ms.assetid: 495598db-a0c9-473b-8184-121a1939b55a
title: 'Элемент Ккритсек:: m_currentOwner (Вксутил. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_currentOwner
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71c88055f5068a5486c1eb6e3ac739235a6b7cde2e8d6b767380160ff12503be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118657217"
---
# <a name="ccritsecm_currentowner-member"></a>Элемент Ккритсек:: m \_ куррентовнер

Идентификатор потока владеющего потока.

## <a name="syntax"></a>Синтаксис


```C++
DWORD m_currentOwner;
```



## <a name="remarks"></a>Remarks

Эта переменная-член определена только в отладочной версии базового класса. [Функции отладки критического раздела](critical-section-debugging-functions.md) используют этот элемент.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>вксутил. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ккритсек**](ccritsec.md)
</dt> </dl>

 

 




