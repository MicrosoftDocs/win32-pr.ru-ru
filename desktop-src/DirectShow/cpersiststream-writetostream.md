---
description: Записывает данные фильтра в заданный поток.
ms.assetid: 1b405050-6cfd-4b69-b449-f00a6ecfac6a
title: Кперсистстреам. Вритетостреам, метод (Пстреам. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPersistStream.WriteToStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 893d58986db92e50cbafefe74676481162808abf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675681"
---
# <a name="cpersiststreamwritetostream-method"></a>Кперсистстреам. Вритетостреам, метод

Записывает данные фильтра в заданный поток.

## <a name="syntax"></a>Синтаксис


```C++
virtual HRESULT WriteToStream(
   IStream *pStream
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстреам* 
</dt> <dd>

Указатель на интерфейс **IStream** , указывающий поток назначения данных фильтра.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение S \_ ОК. Производный класс должен возвращать допустимое значение **HRESULT** .

## <a name="remarks"></a>Комментарии

Версия по умолчанию не записывает ничего; его можно переопределить для записи данных, относящихся к вашему классу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Пстреам. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кперсистстреам**](cpersiststream.md)
</dt> </dl>

 

 




