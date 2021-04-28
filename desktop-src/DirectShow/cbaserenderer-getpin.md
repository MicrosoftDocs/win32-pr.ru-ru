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
ms.openlocfilehash: b7c30767b7cba68931bc1ddde4905c9b7bc2bc29
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119892"
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
| Header<br/>  | <dl> <dt>Ренбасе. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кбасерендерер**](cbaserenderer.md)
</dt> </dl>

 

 




