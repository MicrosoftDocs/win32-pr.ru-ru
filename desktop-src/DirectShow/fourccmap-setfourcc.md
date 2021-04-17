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
ms.openlocfilehash: 435eb209e39ffad29f041e2e117a45d735abffed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689001"
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

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>FourCC. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Фаурккмап**](fourccmap.md)
</dt> </dl>

 

 




