---
description: Кбасерендерер. Жетпин, метод Жетпин извлекает ПИН-код.
ms.assetid: 665e1aaf-4491-4241-94c6-6ea356d7a665
title: Кбасерендерер. Жетпин, метод (Ренбасе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c85b1a33abec4dfd10cf093e8673e270e7df02533846791a5d5d37702b51313
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822705"
---
# <a name="cbaserenderergetpin-method"></a>Кбасерендерер. Жетпин, метод

`GetPin`Метод извлекает ПИН-код.

## <a name="syntax"></a>Синтаксис


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*n* 
</dt> <dd>

Номер указанного пин-кода. Должен равняться нулю.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель [**кбасерендерер:: m \_ пинпутпин**](cbaserenderer-m-pinputpin.md) .

## <a name="remarks"></a>Remarks

Этот метод реализует метод [**кбасефилтер:: жетпин**](cbasefilter-getpin.md) , который является чистым виртуальным в классе **кбасефилтер** . Фильтр поддерживает ровно один ПИН-код (входной ПИН-код). При первом вызове этого метода он создает ПИН-код в качестве нового объекта [**крендереринпутпин**](crendererinputpin.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ренбасе. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




