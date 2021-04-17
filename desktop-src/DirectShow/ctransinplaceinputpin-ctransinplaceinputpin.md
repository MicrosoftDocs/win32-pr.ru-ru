---
description: Метод конструктора.
ms.assetid: db0a3f78-ddb9-43b5-aab5-da2faaebb527
title: Конструктор Ктрансинплацеинпутпин. Ктрансинплацеинпутпин (Трансип. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a801b2c4286f903ef450cac2fd76252f451f9add
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675168"
---
# <a name="ctransinplaceinputpinctransinplaceinputpin-constructor"></a>Ктрансинплацеинпутпин. Ктрансинплацеинпутпин, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CTransInPlaceInputPin(
   TCHAR               *pObjectName,
   CTransInPlaceFilter *pFilter,
   HRESULT             *phr,
   LPCWSTR             pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побжектнаме* 
</dt> <dd>

Строка, содержащая имя отладки объекта. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

</dd> <dt>

*пфилтер* 
</dt> <dd>

Указатель на фильтр, создавший этот ПИН-код, который должен быть объектом [**ктрансинплацефилтер**](ctransinplacefilter.md) .

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода. Перед созданием объекта инициализируйте значение до " \_ ОК". Значение изменяется только в случае возникновения ошибки.

</dd> <dt>

*pName* 
</dt> <dd>

Строка расширенных символов, содержащая имя ПИН-кода.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Параметр *pName* указывает имя ПИН-кода, которое возвращается методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . Однако эта строка не используется для идентификатора ПИН-кода. Идентификатор ПИН-кода для этого класса всегда находится в. Дополнительные сведения см. в разделе [**ктрансформинпутпин:: QueryId**](ctransforminputpin-queryid.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Трансип. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ктрансинплацеинпутпин**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




