---
description: Метод конструктора Ценумпинс. Ценумпинс.
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
ms.openlocfilehash: caa27dfe0190df15be1e41b7128c06249f1ae2b8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099232"
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

## <a name="remarks"></a>Remarks

Если *пенумпинс* имеет **значение NULL**, этот метод инициализирует перечислитель до начала последовательности перечисления. В противном случае он дублирует внутреннее состояние перечислителя, заданного параметром *пенумпинс*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ценумпинс**](cenumpins.md)
</dt> </dl>

 

 




