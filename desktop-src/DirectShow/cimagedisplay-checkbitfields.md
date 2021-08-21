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
ms.openlocfilehash: 44e60b6693dde202cd458cd09495dce9e4bea52ed96a468a8d3dcb6b2370eac4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074178"
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

## <a name="remarks"></a>Remarks

Этот метод проверяет, что цветовая маска для каждого компонента цвета находится в диапазоне от одного до восьми бит, и что каждая цветовая маска является непрерывной последовательностью битов. Этот метод следует вызывать только в том случае, если для элемента **бикомпрессион** задано значение BI \_ битовых полей.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




