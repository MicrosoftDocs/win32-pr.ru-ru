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
ms.openlocfilehash: 870ddbf77d1a29a34703d4b43ee21d02b676e8fafac9ee688384246339465732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073328"
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
| <dl> <dt>**\_ОК**</dt> </dl>      | Success<br/>                |
| <dl> <dt>**\_указатель E**</dt> </dl> | Значение указателя **null**<br/> |



 

## <a name="remarks"></a>Remarks

Время окончания задается переменной-членом [**ксаурцесикинг:: m \_ ртстоп**](csourceseeking-m-rtstop.md) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Ксаурцесикинг**](csourceseeking.md)
</dt> </dl>

 

 




