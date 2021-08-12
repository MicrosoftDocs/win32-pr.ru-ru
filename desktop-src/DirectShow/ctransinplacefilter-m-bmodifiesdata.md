---
description: '\_Переменная-член m бмодифиесдата указывает, изменяет ли фильтр демонстрационные данные, которые получают. Значение задается в конструкторе Ктрансинплацефилтер, но значением по умолчанию является TRUE.'
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Элемент Ктрансинплацефилтер:: m_bModifiesData (Трансип. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7461f7f62a6cbd1fea2ff18f6e8f2e4b73825ea04cb9e3b0a679ee7cf15fef90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654883"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Элемент Ктрансинплацефилтер:: m \_ бмодифиесдата

`m_bModifiesData`Переменная-член указывает, изменяет ли фильтр получаемый образец данных. Значение задается в конструкторе **ктрансинплацефилтер** , но значением по умолчанию является **true**.

## <a name="syntax"></a>Синтаксис


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Remarks

Эта переменная влияет на то, как фильтр согласовывает распределитель. Если значение равно **true**, фильтр не может использовать распределитель только для чтения для обоих подключений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>трансип. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




