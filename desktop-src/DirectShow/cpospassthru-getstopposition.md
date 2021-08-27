---
description: 'Метод Жетстоппоситион извлекает время, когда воспроизведение будет прервано относительно длительности потока. Этот метод реализует метод Имедиасикинг:: Жетстоппоситион.'
ms.assetid: 11486371-da0a-4b83-956b-ef6b92721e74
title: Кпоспасссру. Жетстоппоситион, метод (Ктлутил. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru.GetStopPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f9c6798d03e2935c991e12cded4d85a4972d54e7800d6aa79c70525b10276f91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084074"
---
# <a name="cpospassthrugetstopposition-method"></a>Кпоспасссру. Жетстоппоситион, метод

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

Возвращает значение **HRESULT** из подключенного ПИН-кода.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>ктлутил. h (включает Потоки. h)</dt> </dl>                                                                                   |
| Библиотека<br/> | <dl> <dt>Стрмбасе. lib (розничные сборки); </dt> <dt>Стрмбасд. lib (отладочные сборки)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Класс Кпоспасссру**](cpospassthru.md)
</dt> </dl>

 

 




