---
description: Сведения о методе Кмедиатипе. Кмедиатипе (Мтипе. h). Этот метод использует параметры "мтипе" и "фр".
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметры мтипе и фр
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
ms.openlocfilehash: 12ef9012e59dfce1f45d21aa720ae13bd660f2d8
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "105665019"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>Кмедиатипе. Кмедиатипе-конструктор (Мтипе. h) — параметры мтипе и фр

Метод конструктора.

## <a name="syntax"></a>Синтаксис


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*мтипе* \[ ЗНАЧ\]
</dt> <dd>

Ссылка на структуру [**\_ \_ типа мультимедиа AM**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Конструктор копирует тип мультимедиа в новый объект, включая блок формата, если таковой имеется.

</dd> <dt>

*фр* 
</dt> <dd>

Указатель на переменную, которая получает значение HRESULT. Этот параметр может быть **пустым** указателем. В противном случае перед вызовом конструктора вызывающий объект должен установить значение, равное « \_ ОК». Если конструктор завершается неудачно, ему присваивается значение кода сбоя.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Конструктор вызывает метод [**кмедиатипе:: инитмедиатипе**](cmediatype-initmediatype.md) для инициализации типа мультимедиа.

## <a name="requirements"></a>Требования

| Требование                   | Значение                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header  | Мтипе. h (включение Streams. h)                                                                                     |
| Библиотека | Стрмбасе. lib (розничные сборки); Стрмбасд. lib (отладочные сборки) |

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Кмедиатипе**](cmediatype.md)
</dt> </dl>

 

 




