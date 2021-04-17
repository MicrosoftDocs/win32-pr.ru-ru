---
description: Метод конструктора.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Конструктор Кмедиатипе. Кмедиатипе (Мтипе. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 776d59550d09396cc248937be611f2b4ec3699df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685054"
---
# <a name="cmediatypecmediatype-constructor-mtypeh"></a>Конструктор Кмедиатипе. Кмедиатипе (Мтипе. h)

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaType(
  [ref] const CMediaType &cmtype,
              HRESULT    *phr = NULL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*кмтипе* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на `CMediaType` объект. Конструктор копирует тип мультимедиа в новый объект, включая блок формата, если таковой имеется.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение HRESULT. Этот параметр может быть **пустым** указателем. В противном случае перед вызовом конструктора вызывающий объект должен установить значение, равное « \_ ОК». Если конструктор завершается неудачно, ему присваивается значение кода сбоя.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




