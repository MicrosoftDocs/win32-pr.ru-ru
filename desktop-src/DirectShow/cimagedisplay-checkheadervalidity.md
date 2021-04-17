---
description: Метод Чеккхеадервалидити проверяет структуру БИТМАПИНФОХЕАДЕР. Этот метод полезен только для несжатых типов RGB, а не для сжатых типов или YUV-типов.
ms.assetid: 24b547b6-b730-48b2-9a1b-6e77f9cb1ce1
title: Цимажедисплай. Чеккхеадервалидити, метод (Винутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckHeaderValidity
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 803e8cd1a70c68f3e20c320978e9a350bdf23bdb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105674992"
---
# <a name="cimagedisplaycheckheadervalidity-method"></a>Цимажедисплай. Чеккхеадервалидити, метод

`CheckHeaderValidity`Метод проверяет структуру [**битмапинфохеадер**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) . Этот метод полезен только для несжатых типов RGB, а не для сжатых типов или YUV-типов.

## <a name="syntax"></a>Синтаксис


```C++
BOOL CheckHeaderValidity(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пинпут* 
</dt> <dd>

Указатель на структуру [**видеоинфо**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo) , содержащую структуру **битмапинфохеадер** .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает **значение true** , если **битмапинфохеадер** является допустимым, или **false** в противном случае.

## <a name="remarks"></a>Комментарии

Этот метод проверяет, что размеры изображения не отрицательны; тип сжатия — BI \_ RGB или BI \_ битовых полей; глубина цвета и цветовая маска являются допустимыми; элемент **бипланес** равен единице, а элементы **бисизе** и **бисизеимаже** являются правильными. Он также проверяет наличие типичных ошибок в записях палитры, если таковые имеются.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Винутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




