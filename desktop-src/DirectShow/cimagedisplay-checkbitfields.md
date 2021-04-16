---
description: Метод Чеккбитфиелдс проверяет цветовую маску в структуре ВИДЕОИНФО.
ms.assetid: b03455aa-8d90-4fab-999d-7408d8417021
title: Цимажедисплай. Чеккбитфиелдс, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckBitFields
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ade581dad5e53c2454df52e387653e44d6d4ad2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105656948"
---
# <a name="cimagedisplaycheckbitfields-method"></a>Цимажедисплай. Чеккбитфиелдс, метод

`CheckBitFields`Метод проверяет цветовую маску в структуре [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Синтаксис


```C++
BOOL CheckBitFields(
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

Возвращает **значение true** , если цветовая маска является допустимой, или **значение false** в противном случае.

## <a name="remarks"></a>Комментарии

Этот метод проверяет, что цветовая маска для каждого компонента цвета находится в диапазоне от одного до восьми бит, и что каждая цветовая маска является непрерывной последовательностью битов. Этот метод следует вызывать только в том случае, если для элемента **бикомпрессион** задано значение BI \_ битовых полей.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




