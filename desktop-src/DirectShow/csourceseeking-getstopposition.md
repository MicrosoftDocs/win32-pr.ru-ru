---
description: 'Метод Жетстоппоситион извлекает время, когда воспроизведение останавливается, относительно длительности потока. Этот метод реализует метод Имедиасикинг:: Жетстоппоситион.'
ms.assetid: 83928f62-7acc-43b9-9537-49131ed0b0d4
title: Ксаурцесикинг. Жетстоппоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d9f61ad26c32cfeec285874edfcc26038d57b117
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105688976"
---
# <a name="csourceseekinggetstopposition-method"></a>Ксаурцесикинг. Жетстоппоситион, метод

`GetStopPosition`Метод получает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод [**имедиасикинг:: жетстоппоситион**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getstopposition) .

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetStopPosition(
   LONGLONG *pStop
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пстоп* 
</dt> <dd>

Указатель на переменную, которая получает время окончания в единицах текущего формата времени.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает одно из значений **HRESULT** , перечисленных в следующей таблице.



| Код возврата                                                                               | Описание                       |
|-------------------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>**\_ОК**</dt> </dl>      | Успешно<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl> | Значение указателя **null**<br/> |



 

## <a name="remarks"></a>Комментарии

Время окончания задается переменной-членом [**ксаурцесикинг:: m \_ ртстоп**](csourceseeking-m-rtstop.md) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ктлутил. h (включение Streams. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




