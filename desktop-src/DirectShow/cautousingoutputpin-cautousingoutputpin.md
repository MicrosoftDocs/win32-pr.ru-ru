---
description: Метод конструктора. Конструктор получает доступ к указанному ПИН-коду.
ms.assetid: 518d41aa-8361-4769-aa9b-14676b676d6f
title: Конструктор Каутаусингаутпутпин. Каутаусингаутпутпин (Амфилтер. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin.CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 94bafcdcb6e44a07afdccea382d783c20a9ad2ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657855"
---
# <a name="cautousingoutputpincautousingoutputpin-constructor"></a>Каутаусингаутпутпин. Каутаусингаутпутпин, конструктор

Метод конструктора. Конструктор получает доступ к указанному ПИН-коду.

## <a name="syntax"></a>Синтаксис


```C++
CAutoUsingOutputPin(
   CDynamicOutputPin *pOutputPin,
   HRESULT           *phr
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*паутпутпин* 
</dt> <dd>

Указатель на объект [**кдинамикаутпутпин**](cdynamicoutputpin.md) .

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, содержащую значение **HRESULT** . Значение должно быть равно "S" \_ .

</dd> </dl>

## <a name="remarks"></a>Комментарии

При возврате из метода значение *\* фр* указывает на успешное или неуспешное завершение метода.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Амфилтер. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Каутаусингаутпутпин**](cautousingoutputpin-cautousingoutputpin.md)
</dt> </dl>

 

 




