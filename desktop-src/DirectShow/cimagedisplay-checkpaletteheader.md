---
description: Метод Чеккпалеттехеадер проверяет записи палитры в структуре ВИДЕОИНФО.
ms.assetid: bc18cbe6-0446-43a6-a50c-e587815b789d
title: Цимажедисплай. Чеккпалеттехеадер, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckPaletteHeader
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6378a93ffced86546b8e95071e7f9bdc1398cdd1831aa18d41d62c6ea97caff0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087294"
---
# <a name="cimagedisplaycheckpaletteheader-method"></a>Цимажедисплай. Чеккпалеттехеадер, метод

`CheckPaletteHeader`Метод проверяет записи палитры в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL CheckPaletteHeader(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинпут* 
</dt> <dd>

Указатель на структуру **видеоинфо** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если записи палитры допустимы, или **false** в противном случае.

## <a name="remarks"></a>Remarks

Если формат изображения не палеттизед, метод проверяет, что **биклрусед** равен нулю. В противном случае метод проверяет, что флаг **бикомпрессион** — это BI \_ RGB; **биклримпортант** не превышает **биклрусед**; и число записей в палитре не превышает максимальное значение, учитывая глубину цвета.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




