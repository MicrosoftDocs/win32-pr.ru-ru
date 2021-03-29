---
description: Метод Каунтпрефиксбитс вычисляет количество нулевых битов в начале указанного битового поля.
ms.assetid: 36fc5c5f-dc64-4588-9130-1b0740d03be1
title: Цимажедисплай. Каунтпрефиксбитс, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CountPrefixBits
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4333e1b0826b4fac7bfff463531b5d2e10704418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657657"
---
# <a name="cimagedisplaycountprefixbits-method"></a>Цимажедисплай. Каунтпрефиксбитс, метод

`CountPrefixBits`Метод вычисляет количество нулевых битов в начале указанного битового поля.

## <a name="syntax"></a>Синтаксис


```C++
DWORD CountPrefixBits(
   const DWORD Field
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Поле* 
</dt> <dd>

Задает битовое поле в виде значения **типа DWORD** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает число нулей, предшествующих первому 1 биту, или 0x80000000, если все биты равны нулю.

## <a name="remarks"></a>Комментарии

Этот метод полезен для работы с цветовыми масками в структурах [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




