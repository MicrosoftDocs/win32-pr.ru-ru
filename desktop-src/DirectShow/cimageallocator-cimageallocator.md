---
description: Метод конструктора Цимажеаллокатор. Цимажеаллокатор.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Конструктор Цимажеаллокатор. Цимажеаллокатор (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085762"
---
# <a name="cimageallocatorcimageallocator-constructor"></a>Цимажеаллокатор. Цимажеаллокатор, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфилтер* 
</dt> <dd>

Указатель на фильтр-владелец.

</dd> <dt>

*pName* 
</dt> <dd>

Указатель на строку, содержащую имя отладки распределителя. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на значение **HRESULT** . Перед созданием объекта задайте для него значение " \_ ОК". Если конструктор завершается неудачно, ему присваивается значение кода ошибки.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажеаллокатор**](cimageallocator.md)
</dt> </dl>

 

 




