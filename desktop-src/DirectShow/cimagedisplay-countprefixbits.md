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
ms.openlocfilehash: 510ac01baab55fbf45e3441296018426335a8f50061f06400872fd7275d3e273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108484"
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

## <a name="remarks"></a>Remarks

Этот метод полезен для работы с цветовыми масками в структурах [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




