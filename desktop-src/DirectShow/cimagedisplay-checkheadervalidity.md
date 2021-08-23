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
ms.openlocfilehash: 25c8ce12f7e383e04942184e3897d0ddc52700a1a621844719d94f54f60203ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119652364"
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

## <a name="remarks"></a>Remarks

Этот метод проверяет, что размеры изображения не отрицательны; тип сжатия — BI \_ RGB или BI \_ битовых полей; глубина цвета и цветовая маска являются допустимыми; элемент **бипланес** равен единице, а элементы **бисизе** и **бисизеимаже** являются правильными. Он также проверяет наличие типичных ошибок в записях палитры, если таковые имеются.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>винутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Цимажедисплай**](cimagedisplay.md)
</dt> </dl>

 

 




