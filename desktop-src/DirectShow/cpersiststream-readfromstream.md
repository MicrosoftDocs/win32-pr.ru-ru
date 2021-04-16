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
ms.openlocfilehash: ce6c037fbce9fbaeabf7491b1b840000f67e25d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668667"
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

## <a name="remarks"></a>Комментарии

Версия по умолчанию не считывает ничего; его можно переопределить для чтения данных, относящихся к вашему классу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пстреам. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




