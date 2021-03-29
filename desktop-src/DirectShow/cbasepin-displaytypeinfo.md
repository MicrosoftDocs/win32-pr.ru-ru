---
description: Метод Дисплайтипеинфо отображает сведения о типе носителя во время отладки.
ms.assetid: fd10d37b-57f5-4246-8ca3-f4bc59911445
title: Кбасепин. Дисплайтипеинфо, метод (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.DisplayTypeInfo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 681e424505bb2ff840ac5beaa48431f17a5d177b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657514"
---
# <a name="cbasepindisplaytypeinfo-method"></a>Кбасепин. Дисплайтипеинфо, метод

`DisplayTypeInfo`Метод отображает сведения о типе носителя во время отладки.

## <a name="syntax"></a>Синтаксис


```C++
void DisplayTypeInfo(
         IPin       *pPin,
   const CMediaType *pmt
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ппин* 
</dt> <dd>

Не обрабатывается.

</dd> <dt>

*состоит* 
</dt> <dd>

Указатель на объект [**кмедиатипе**](cmediatype.md) , указывающий тип мультимедиа.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Комментарии

В отладочных сборках этот метод вызывает функцию [**дбглог**](dbglog.md) для вывода указанного типа мультимедиа. В розничных сборках этот метод не выполняет никаких действий.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




