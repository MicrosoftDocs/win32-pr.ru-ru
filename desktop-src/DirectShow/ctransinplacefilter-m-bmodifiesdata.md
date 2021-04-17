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
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657329"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a>Элемент Ктрансинплацефилтер:: m \_ бмодифиесдата

`m_bModifiesData`Переменная-член указывает, изменяет ли фильтр получаемый образец данных. Значение задается в конструкторе **ктрансинплацефилтер** , но значением по умолчанию является **true**.

## <a name="syntax"></a>Синтаксис


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a>Примечания

Эта переменная влияет на то, как фильтр согласовывает распределитель. Если значение равно **true**, фильтр не может использовать распределитель только для чтения для обоих подключений.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацефилтер**](ctransinplacefilter.md)
</dt> </dl>

 

 




