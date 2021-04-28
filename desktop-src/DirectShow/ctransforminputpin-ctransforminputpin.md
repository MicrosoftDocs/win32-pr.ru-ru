---
description: Метод конструктора Ктрансформинпутпин. Ктрансформинпутпин.
ms.assetid: 097dce19-b430-42d6-8914-68350c7eca40
title: Конструктор Ктрансформинпутпин. Ктрансформинпутпин (Трансфрм. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4e893b4e1c7d4f396644a468d3d71fa3046fb712
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095052"
---
# <a name="ctransforminputpinctransforminputpin-constructor"></a>Ктрансформинпутпин. Ктрансформинпутпин, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CTransformInputPin(
   TCHAR            *pObjectName,
   CTransformFilter *pTransformFilter,
   HRESULT          *phr,
   LPCWSTR          pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побжектнаме* 
</dt> <dd>

Строка, содержащая имя отладки объекта. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

</dd> <dt>

*птрансформфилтер* 
</dt> <dd>

Указатель на фильтр, создавший этот ПИН-код, который должен быть объектом [**ктрансформфилтер**](ctransformfilter.md) .

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода. Перед созданием объекта инициализируйте значение до " \_ ОК". Значение изменяется только в случае возникновения ошибки.

</dd> <dt>

*pName* 
</dt> <dd>

Строка расширенных символов, содержащая имя ПИН-кода.

</dd> </dl>

## <a name="remarks"></a>Remarks

Параметр *pName* указывает имя ПИН-кода, которое возвращается методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Однако строка не используется для идентификатора ПИН-кода. Идентификатор ПИН-кода для этого класса всегда имеет значение "in". Дополнительные сведения см. в разделе [**QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансфрм. h (включение Streams. h)</dt> </dl>                                                                                  |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



 

 




