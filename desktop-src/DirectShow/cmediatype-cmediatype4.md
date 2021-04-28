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
ms.openlocfilehash: dd91252920c74d45e4218be3c3d03249a116bfcf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095422"
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
| Header<br/>  | <dl> <dt>Мтипе. h (включение Streams. h)</dt> </dl>                                                                                     |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




