---
description: Метод конструктора Ценуммедиатипес. Ценуммедиатипес.
ms.assetid: fae2e05c-3f7b-4511-9b9d-5a37ea03f851
title: Конструктор Ценуммедиатипес. Ценуммедиатипес (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes.CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d243ed25cc48c5d30d467f97e2ec20e1f0f2b58
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095682"
---
# <a name="cenummediatypescenummediatypes-constructor"></a>Ценуммедиатипес. Ценуммедиатипес, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CEnumMediaTypes(
   CBasePin        *pPin,
   CEnumMediaTypes *pEnumMediaTypes
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Указатель на ПИН-код, на котором должно быть выполнено перечисление.

</dd> <dt>

*пенуммедиатипес* 
</dt> <dd>

Указатель на интерфейс [**иенуммедиатипес**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) перечислителя, который необходимо клонировать, или **значение NULL**.

</dd> </dl>

## <a name="remarks"></a>Remarks

Если *пенуммедиатипес* имеет **значение NULL**, этот метод инициализирует перечислитель до начала последовательности перечисления. В противном случае он дублирует внутреннее состояние перечислителя, заданного параметром *пенуммедиатипес*.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ценуммедиатипес**](cenummediatypes.md)
</dt> </dl>

 

 




