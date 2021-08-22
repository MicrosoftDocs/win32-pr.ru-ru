---
description: Задает часть FOURCC объекта Фаурккмап.
ms.assetid: cc821e39-e565-4255-a289-2c9507d43433
title: 'Метод Фаурккмап:: Сетфауркк (FourCC. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FOURCCMap.SetFOURCC
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 03ac14c7174fde7184bfdbfbb5d82d3fc1288d46ff37158bbbab146c34db5ed9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536834"
---
# <a name="fourccmapsetfourcc-method"></a>Метод Фаурккмап:: Сетфауркк

Задает часть **FourCC** объекта [**фаурккмап**](fourccmap.md) .

## <a name="syntax"></a>Синтаксис


```C++
void SetFOURCC(
   const GUID *pguid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пгуид* 
</dt> <dd>

Указатель на возвращенный глобальный уникальный идентификатор (**GUID**) объекта **фаурккмап** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Нет возвращаемого значения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>Fourcc. h (включает Потоки. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Фаурккмап**](fourccmap.md)
</dt> </dl>

 

 




