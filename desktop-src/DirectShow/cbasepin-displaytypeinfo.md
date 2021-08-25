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
ms.openlocfilehash: 10b4535950a46fa55aba0ea7d808a075186f074cc829be0d3225dc887512ad47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119916454"
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

## <a name="remarks"></a>Remarks

В отладочных сборках этот метод вызывает функцию [**дбглог**](dbglog.md) для вывода указанного типа мультимедиа. В розничных сборках этот метод не выполняет никаких действий.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>амфилтер. h (включает Потоки. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасепин**](cbasepin.md)
</dt> </dl>

 

 




