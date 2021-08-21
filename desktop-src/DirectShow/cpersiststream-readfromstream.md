---
description: Считывает данные фильтра из заданного потока.
ms.assetid: 009f4812-8cc6-436a-9553-3a3161d5e992
title: Кперсистстреам. Реадфромстреам, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.ReadFromStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 39f40871e12a069045197d0cc61970c7d7f88c784f6b0873c294727b75121ae6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073648"
---
# <a name="cpersiststreamreadfromstream-method"></a>Кперсистстреам. Реадфромстреам, метод

Считывает данные фильтра из заданного потока.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT ReadFromStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстреам* 
</dt> <dd>

Указатель на интерфейс **IStream** , из которого считываются данные.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК. Производный класс должен возвращать допустимое значение **HRESULT** .

## <a name="remarks"></a>Remarks

Версия по умолчанию не считывает ничего; его можно переопределить для чтения данных, относящихся к вашему классу.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>пстреам. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




