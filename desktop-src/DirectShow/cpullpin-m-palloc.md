---
description: '\_Переменная-член m паллок является указателем на интерфейс имемаллокатор распределителя памяти.'
ms.assetid: a3be5982-83f0-4552-9bcd-85da4a4918ff
title: 'Элемент Кпуллпин:: m_pAlloc (Пуллпин. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAlloc
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e9945bd7b5f3c5b54f0ef578c2b012d0e56935d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669053"
---
# <a name="cpullpinm_palloc-member"></a>Элемент Кпуллпин:: m \_ паллок

`m_pAlloc`Переменная-член является указателем на интерфейс [**имемаллокатор**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) распределителя памяти.

## <a name="syntax"></a>Синтаксис


```C++
IMemAllocator *m_pAlloc;
```



## <a name="remarks"></a>Примечания

Метод [**кпуллпин::D еЦидеаллокатор**](cpullpin-decideallocator.md) задает эту переменную члена.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пуллпин. h</dt> </dl>                                                                                                       |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кпуллпин**](cpullpin.md)
</dt> </dl>

 

 




