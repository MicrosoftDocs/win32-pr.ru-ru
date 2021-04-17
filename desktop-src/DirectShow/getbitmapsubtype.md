---
description: Функция Жетбитмапсубтипе возвращает идентификатор GUID подтипа носителя для указанного точечного рисунка.
ms.assetid: 0af8a64b-8d3c-4308-9fd6-174864a1ca26
title: Функция Жетбитмапсубтипе (Вксутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetBitmapSubtype
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7ba12ffcd1b50b920f28e1969444a2d31a9d073d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675526"
---
# <a name="getbitmapsubtype-function"></a>Функция Жетбитмапсубтипе

`GetBitmapSubtype`Функция возвращает **идентификатор GUID** подтипа носителя для указанного точечного рисунка.

## <a name="syntax"></a>Синтаксис


```C++
const GUID GetBitmapSubtype(
   const BITMAPINFOHEADER *pHeader
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*феадер* 
</dt> <dd>

Указатель на структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **GUID** подтипа носителя.

## <a name="remarks"></a>Комментарии

Для несжатых типов RGB эта функция сопоставляет поле **бибиткаунт** с подтипом. Для типов сжатых видео эта функция использует класс [**фаурккмап**](fourccmap.md) для соответствия поля **бикомпрессион** подтипу.

Если функция не может соответствовать формату подтипа, возвращаемое значение — GUID \_ null.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Вксутил. h (включение Streams. h)</dt> </dl>                                                                                    |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции видео и изображений](video-and-image-functions.md)
</dt> </dl>

 

 




