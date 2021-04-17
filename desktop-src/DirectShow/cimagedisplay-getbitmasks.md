---
description: Метод ВИДЕОИНФО извлекает цветовую маску для указанного формата.
ms.assetid: 72a9ba44-96de-4fff-a3fb-675d3dd080d8
title: Метод Цимажедисплай. с битовой маски (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.GetBitMasks
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a2defe5e80a0d7311adcd19dca67119019623993
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105658002"
---
# <a name="cimagedisplaygetbitmasks-method"></a>Цимажедисплай..., метод

`GetBitMasks`Метод извлекает цветовую маску для указанного формата [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) .

## <a name="syntax"></a>Синтаксис


```C++
const DWORD* GetBitMasks(
   const VIDEOINFO *pVideoInfo
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пвидеоинфо* 
</dt> <dd>

Указатель на структуру **видеоинфо** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает массив из трех значений **типа DWORD** .

## <a name="remarks"></a>Комментарии

Если элемент **бикомпрессион** является BI \_ битовых полей, метод возвращает указатель на цветовую маску, переданную в элементе **двбитмаскс** . Если элемент **бикомпрессион** является BI \_ RGB, метод возвращает цветовые маски, соответствующие глубине цвета. Если метод завершается ошибкой (например, глубина разрядности меньше 16), метод возвращает массив {0,0,0} .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




