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
ms.openlocfilehash: 54c4f401d2e75aeb35ffc19d26690fa04a769c27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679741"
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

## <a name="remarks"></a>Комментарии

Если формат изображения не палеттизед, метод проверяет, что **биклрусед** равен нулю. В противном случае метод проверяет, что флаг **бикомпрессион** — это BI \_ RGB; **биклримпортант** не превышает **биклрусед**; и число записей в палитре не превышает максимальное значение, учитывая глубину цвета.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




