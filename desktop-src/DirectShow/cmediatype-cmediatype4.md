---
description: Конструктор Кмедиатипе. Кмедиатипе (Мтипе. h) — метод-конструктор.
ms.assetid: 35198320-d028-42d4-823f-4f8346d8f977
title: Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметры кмтипе и фр
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
ms.openlocfilehash: 2f686d1338073c65ce3e5bc3871ae8f4a5b9102e78d7678d5bcf6f77a565397d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792954"
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

## <a name="remarks"></a>Remarks

Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>мтипе. h (включает Потоки. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




