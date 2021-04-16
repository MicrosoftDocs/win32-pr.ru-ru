---
description: Метод конструктора.
ms.assetid: 9078b2f5-b11e-4780-8143-6738e9df4f4b
title: Конструктор Ксаурцестреам. Ксаурцестреам (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a8671e939364d1c0cd22796b1518313002b5eb33
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657167"
---
# <a name="csourcestreamcsourcestream-constructor"></a>Ксаурцестреам. Ксаурцестреам, конструктор

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CSourceStream(
   TCHAR   *pObjectName,
   HRESULT *phr,
   CSource *pms,
   LPCWSTR pName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*побжектнаме* 
</dt> <dd>

Указатель на строку, содержащую имя отладки ПИН-кода.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение **HRESULT** , указывающее на успешное выполнение или ошибку метода. Перед созданием объекта инициализируйте значение до " \_ ОК". Значение изменяется только в случае возникновения ошибки.

</dd> <dt>

*утверждены руководителем* 
</dt> <dd>

Указатель на фильтр [**ксаурце**](csource.md) , который создал этот ПИН-код.

</dd> <dt>

*pName* 
</dt> <dd>

Указатель на строку, содержащую имя ПИН-кода.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Строка, заданная в параметре *побжектнаме* , используется только в целях отладки. Дополнительные сведения см. в разделе [**кбасеобжект**](cbaseobject.md).

Строка, заданная в параметре *pName* , является именем, возвращаемым методом [**Ипин:: куерипининфо**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) . `CSourceStream`Класс не использует это имя для идентификатора ПИН-кода, возвращаемого методом [**ксаурцестреам:: QueryId**](csourcestream-queryid.md) . Вместо этого **QueryId** вычисляет идентификатор ПИН-кода на основе PIN-кода. (Идентификаторы ПИН-кода поддерживают сохраняемость графа. Дополнительные сведения см. в разделе [**Ипин:: QueryId**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid).

Конструктор автоматически добавляет ПИН-код в фильтр владельца путем вызова [**ксаурце:: аддпин**](csource-addpin.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Source. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцестреам**](csourcestream.md)
</dt> </dl>

 

 




