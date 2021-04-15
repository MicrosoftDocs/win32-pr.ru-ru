---
description: Метод конструктора.
ms.assetid: f696e433-b051-4de0-80e5-f9cd31fd0f23
title: Конструктор Ценумпинс. Ценумпинс (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins.CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 536782de6992acfc1613d5866f13af658fba6e71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668825"
---
# <a name="cenumpinscenumpins-constructor"></a>Ценумпинс. Ценумпинс, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CEnumPins(
   CBaseFilter *pFilter,
   CEnumPins   *pEnumPins
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пфилтер* 
</dt> <dd>

Указатель на фильтр, по которому производится перечисление ПИН-кодов.

</dd> <dt>

*пенумпинс* 
</dt> <dd>

Указатель на интерфейс [**иенумпинс**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) перечислителя, который необходимо клонировать, или **значение NULL**.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Если *пенумпинс* имеет **значение NULL**, этот метод инициализирует перечислитель до начала последовательности перечисления. В противном случае он дублирует внутреннее состояние перечислителя, заданного параметром *пенумпинс*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ценумпинс**](cenumpins.md)
</dt> </dl>

 

 




